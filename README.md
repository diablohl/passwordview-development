##8/17/2016: As of about an hour ago, this library is deprecated!  
Support for password visibility is now included in the 
[Design Support Library](https://developer.android.com/topic/libraries/support-library/revisions.html) in [TextInputLayout](https://developer.android.com/reference/android/support/design/widget/TextInputLayout.html). :tada:


#PasswordView [deprecated]

:eyes: "All eyes, yeah I see 'em" — [Yo Gotti, Down in the DM](https://genius.com/Yo-gotti-down-in-the-dm-lyrics)

`compile 'com.xwray:passwordview:1.0'`

### Drop-in Android password view for the new material design spec
    <com.xwray.passwordview.PasswordView
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:hint="@string/password_hint" />

<img src="http://i.imgur.com/k6McHxN.png" width="400px" /><img src="http://i.imgur.com/oO3jBPP.png" width="400px" />

### Toggle password visibility
Touch the "eye" icon to toggle between traditional and visible password states.

### Custom typeface support
In the spec, the password field is pictured in Roboto. I really liked how this looked, so, I made PasswordView support custom typefaces!  If you set one, it will stay. If you don't, the default is still `monospace` — no worries.

`passwordView.setTypeface(roboto);`

### Optional strikethrough
By default, PasswordView adheres exactly to the spec, using 54% / 38% opacity for the visibility icon (or 50% / 100% for light on dark themes).  The visibility icon is drawn using `textColorPrimary` and its opacity values (dark or light) are determined dynamically.

If you find opacity too subtle (insert eye roll :eyes:), you can use the visibility icon with a strikethrough instead.
(idea credit, [@thekeeperofpie](https://github.com/TheKeeperOfPie))

`app:useStrikeThrough="true"` /  `passwordView.setUseStrikethrough(true)`
