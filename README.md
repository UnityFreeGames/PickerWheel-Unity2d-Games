# Easy Fortune Spin Wheel UI
<br />
A powerful,Customizable, and esay-to-use Spin Wheel UI for Unity
<br />
<br />
Video tutorial :https://youtu.be/Apf4JbBbVfc<br />
Group :https://t.me/Unity_Tutorial_Games<br /><br />
🎨Game Artist : https://t.me/maria_artgallery<br />
🎨Game Artist : https://instagram.com/mariaartpro<br /><br />
PLAY : https://play.google.com/store/apps/details/Fun_Arcade_Player_Mini_Games?id=com.coconika.reminder<br />
Site : https://www.rarecreativities.com/game-design <br /><br />

![banner32](https://user-images.githubusercontent.com/83016119/220857805-df32f682-8a66-4de8-8fb9-610209d68c96.png)


■ How to use? :
1. Add DoTween package: http://dotween.demigiant.com/download.php
2. Add EasyUI_PickerWheel package.
3. Create a Canvas and addPickerWheel prefab to it.
Assets/PickerWheel/Prefabs/PickerWheel.prefab

4. Create a Demo.cs script.
5. Add EasyUI.PickerWheelUI namespace.
6. Demo.cs :
<br /><br />
<pre><span class="pl-k">using</span> <span class="pl-en">UnityEngine</span>;
<span class="pl-k">using</span> <span class="pl-en">EasyUI</span>.<span class="pl-en">PickerWheelUI</span>;   <span class="pl-c"><span class="pl-c">//</span>required</span>

<span class="pl-k">public</span> <span class="pl-k">class</span> <span class="pl-en">Demo</span> : <span class="pl-en">MonoBehaviour</span> {
	<span class="pl-c"><span class="pl-c">//</span> Reference to the PickerWheel GameObject (step 3):</span>
	[<span class="pl-en">SerializeField</span>] <span class="pl-k">private</span> <span class="pl-en">PickerWheel</span> <span class="pl-en">pickerWheel</span>;
	
	<span class="pl-k">private</span> <span class="pl-k">void</span> <span class="pl-en">Start</span> () {
		<span class="pl-c"><span class="pl-c">//</span> Start spinning:</span>
		<span class="pl-smi">pickerWheel</span>.<span class="pl-en">Spin</span> ();
	}
}</pre>
<br /><br />
■ Wheel Events : OnSpinStart  and OnSpinEnd  :
<br /><br />
<pre><span class="pl-k">using</span> <span class="pl-en">UnityEngine</span>;
<span class="pl-k">using</span> <span class="pl-en">EasyUI</span>.<span class="pl-en">PickerWheelUI</span>;

<span class="pl-k">public</span> <span class="pl-k">class</span> <span class="pl-en">Demo</span> : <span class="pl-en">MonoBehaviour</span> {
	[<span class="pl-en">SerializeField</span>] <span class="pl-k">private</span> <span class="pl-en">PickerWheel</span> <span class="pl-en">pickerWheel</span>;
	
	<span class="pl-k">private</span> <span class="pl-k">void</span> <span class="pl-en">Start</span> () {
		<span class="pl-smi">pickerWheel</span>.<span class="pl-en">OnSpinStart</span> (() <span class="pl-k">=&gt;</span>  {
			<span class="pl-smi">Debug</span>.<span class="pl-en">Log</span> (<span class="pl-s"><span class="pl-pds">"</span>Spin start...<span class="pl-pds">"</span></span>));
		});

		<span class="pl-smi">pickerWheel</span>.<span class="pl-en">OnSpinEnd</span> (<span class="pl-en">wheelPiece</span> <span class="pl-k">=&gt;</span> {
			<span class="pl-smi">Debug</span>.<span class="pl-en">Log</span> (<span class="pl-s"><span class="pl-pds">"</span>Spin end :<span class="pl-pds">"</span></span>) ;
			<span class="pl-smi">Debug</span>.<span class="pl-en">Log</span> (<span class="pl-s"><span class="pl-pds">"</span>Index   : <span class="pl-pds">"</span></span><span class="pl-k">+</span><span class="pl-smi">wheelPiece</span>.<span class="pl-smi">Index</span>);
			<span class="pl-smi">Debug</span>.<span class="pl-en">Log</span> (<span class="pl-s"><span class="pl-pds">"</span>Chance  : <span class="pl-pds">"</span></span><span class="pl-k">+</span><span class="pl-smi">wheelPiece</span>.<span class="pl-smi">Chance</span>);
			<span class="pl-smi">Debug</span>.<span class="pl-en">Log</span> (<span class="pl-s"><span class="pl-pds">"</span>Label   : <span class="pl-pds">"</span></span><span class="pl-k">+</span><span class="pl-smi">wheelPiece</span>.<span class="pl-smi">Label</span>);
			<span class="pl-smi">Debug</span>.<span class="pl-en">Log</span> (<span class="pl-s"><span class="pl-pds">"</span>Amount  : <span class="pl-pds">"</span></span><span class="pl-k">+</span><span class="pl-smi">wheelPiece</span>.<span class="pl-smi">Amount</span>);
		});

		<span class="pl-smi">pickerWheel</span>.<span class="pl-en">Spin</span> ();
	}
}</pre>
