## Soft keyboard

Supposed that we tap on `EditText A` and a soft keyboard appear:
- Soft keyboard will be dismissed when `EditText A` is destroyed (e.g. via calling `removeView`, fragment/activity that `EditText A` belongs being destroyed etc).
- Changing `EditText A` visibility will not dismiss soft keyboard.
- While soft keyboard for `EditText A` is showing, calling `requestFocus()` on another `EditText B` will cause soft keyboard input to go to `EditText B`.