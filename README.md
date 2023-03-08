# Easy Fortune Spin Wheel UI
<br />
A powerful,Customizable, and esay-to-use Spin Wheel UI for Unity
<br />
<br />
Video tutorial :https://youtu.be/Yd8jYG9yx_E<br />
Group :https://t.me/Unity_Tutorial_Games<br /><br />
🎨Game Artist : https://instagram.com/mariaartpro  <br /><br />
Google Play: https://play.google.com/store/apps/dev?id=7696656736256201466<br />

<h2 tabindex="-1" dir="auto"><a id="user-content-️-donate" class="anchor" aria-hidden="true" href="#️-donate"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a><g-emoji class="g-emoji" alias="heart" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/2764.png">❤️</g-emoji> Donate</h2>

<p dir="auto"><a href="https://www.paypal.com/donate/?hosted_button_id=F86F4AB65QNYL" title="https://paypal.me/Antoni" rel="nofollow"><img align="left" height="50" src="https://camo.githubusercontent.com/59cfbcf1ae58c3d6f862b1633f575920df6db1ac8974973b5e7f341a388b292d/68747470733a2f2f7777772e6d65646961666972652e636f6d2f636f6e766b65792f373264632f697a3738797337767466736c3935377a672e6a7067" alt="Paypal" data-canonical-src="https://www.mediafire.com/convkey/72dc/iz78ys7vtfsl957zg.jpg" style="max-width: 100%;"></a></p>

<br /><br />

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
