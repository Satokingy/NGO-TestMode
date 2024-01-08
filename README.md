# NGO-TestMode
NEEDY GIRL OVERDOSEでテストモードに入るためのメモ
![test](https://github.com/Satokingy/NGO-TestMode/assets/66546019/2f43a962-549e-4bd4-bd2c-f9a4710d2b50.png)

## 注意
全エンディングなどが見られてしまうため、必ずゲームをクリアしてから改造を行ってください。<br>
また、テストモードで遊んでいるところをネットにアップロードしないでください。

### やり方
dnspyで「NEEDY GIRL OVERDOSE\Windose_Data\Managed\Assembly-CSharp.dll」を開く。バックアップを取るといつでも元のファイルに戻せるのでおすすめ<br>
ngov3.Bootで検索をかけて上にあるpublic void Awake()で右クリックしてEdit Method<br>

```
using System;
using System.Collections.Generic;
using Cysharp.Threading.Tasks;
using DG.Tweening;
using TMPro;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

namespace ngov3
{
	// Token: 0x020008BD RID: 2237
	public partial class Boot : MonoBehaviour
	{
		// Token: 0x06002621 RID: 9761 RVA: 0x00013F2E File Offset: 0x0001212E
		public void Awake()
		{
			SingletonMonoBehaviour<Settings>.Instance.saveNumber = 4;
			SceneManager.LoadScene("Window2DTestScene");
		}
	}
}
```
次のように編集<br>
Compileを押してFile→Save All→OK で完了。<br>
後は普通にゲームを起動するだけ
