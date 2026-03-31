# level-up-rebuttal

**Table 1**

| Setting | Method | Model | Dataset | #Source | #Transitional | #Per level |
|---------|--------|-------|---------|---------|---------------|------------|
| Math | In-distribution | Qwen2.5-1.5B-Base | GSM8k | 6500 | 2092 | 675, 462, 272, 289, 394 |
| Math | Distillation | Qwen2.5-0.5B-Base | GSM8k | 6500 | 5442 | 2181, 2113, 693, 255 |
| Math | Neo-transitional | Qwen2.5-0.5B-Base | Orca-formatted | 5000 | 539 | 174, 139, 114, 56, 56 |
| Chess | In-distribution | Maia-2 | Puzzles | ~5.8M | 180,000 | 20,000 |
| Chess | Transfer | Maia-2 | Game Positions | ~300B | 180,000 | 20,000 |

**Table 2**

| Dataset | Phase | Model | Runtime |
|---------|-------|-------|---------|
| GSM8k | Collect checkpoints | Qwen2.5-1.5B-Base | 25 min 22 sec |
| Transitional/GSM8k | Curriculum (per method/baseline) | Qwen2.5-1.5B-Base | 8 min 5 sec |

**Table 3**

<table>
  <tr>
    <td colspan="2"><b>MATH Avg@8 ACC (5+ trials)</b></td>
    <td colspan="3"><b>Transitional Problems</b></td>
    <td colspan="4"><b>Full training dataset</b></td>
  </tr>
  <tr>
    <td>Setting</td>
    <td>Model</td>
    <td>Level-down</td>
    <td>IID</td>
    <td><b>Level-up</b></td>
    <td>IID</td>
    <td>Length</td>
    <td>Steps</td>
    <td><i>C-score equivalent</i></td>
  </tr>
  <tr>
    <td>In-distribution</td>
    <td>Qwen2.5-1.5B-Base</td>
    <td>43.18</td>
    <td>47.43</td>
    <td><b>49.18</b></td>
    <td>44.35</td>
    <td>40.27</td>
    <td>46.36</td>
    <td><i>43.84</i></td>
  </tr>
  <tr>
    <td>Distillation series</td>
    <td>Qwen2.5-0.5B-Base</td>
    <td>13.01</td>
    <td>16.67</td>
    <td><b>21.4</b></td>
    <td>14.61</td>
    <td>20.18</td>
    <td>12.97</td>
    <td><i>13.87</i></td>
  </tr>
  <tr>
    <td>k-shot series</td>
    <td>Qwen2.5-1.5B-Base</td>
    <td>46.66</td>
    <td>47.46</td>
    <td><b>48.63</b></td>
    <td>43.68</td>
    <td>42.67</td>
    <td>43.32</td>
    <td><i>40.74</i></td>
  </tr>
  <tr>
    <td colspan="2"><b>CHESS Accuracy (10 trials)</b></td>
    <td>Level-down</td>
    <td>IID</td>
    <td><b>Level-up</b></td>
    <td>Legal Moves</td>
    <td>Soln. Length</td>
    <td>Rating</td>
    <td><i>C-score equivalent</i></td>
  </tr>
  <tr>
    <td>Chess Puzzles</td>
    <td>Maia-2</td>
    <td>27.1</td>
    <td>28.4</td>
    <td><b>31.2</b></td>
    <td>17.1</td>
    <td>17.3</td>
    <td>17.1</td>
    <td><i>18.0</i></td>
  </tr>
</table>