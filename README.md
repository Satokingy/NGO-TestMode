# NGO-TestMode
NEEDY GIRL OVERDOSEでテストモードに入るためのメモ

## 注意
全エンディングなどが見られてしまうため、必ずゲームをクリアしてから改造を行ってください。

###やり方
dnspyで「NEEDY GIRL OVERDOSE\Windose_Data\Managed\Assembly-CSharp.dll」を開く。バックアップを取るといつでも元のファイルに戻せるのでおすすめ
ngov3.Bootで検索をかけて上にあるpublic void Awake()で右クリックしてEdit Method

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
次のように編集
Compileを押してFile→Save All→OK で完了。
後は普通にゲームを起動するだけ
