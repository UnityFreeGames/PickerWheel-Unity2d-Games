# Easy Fortune Spin Wheel UI
<br />
A powerful,Customizable, and esay-to-use Spin Wheel UI for Unity
<br />
<br />
Video tutorial :https://youtu.be/i3PIGiBmtdA<br />
Group :https://t.me/Unity_Free_Source<br /><br />
🎨Game Artist : https://t.me/maria_artgallery👱🏻‍♀️<br />
🎨Game Artist : https://twitter.com/Mariaartist__👱🏻‍♀️<br />
🎨Game Artist : http://instagram.com/mariartist__👱🏻‍♀️<br /><br />
PLAY : https://play.google.com/store/apps/details/Fun_Arcade_Player_Mini_Games?id=com.coconika.reminder<br />
Site : https://www.rarecreativities.com/game-design <br /><br />

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
