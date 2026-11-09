# Crestron to Q-SYS Map

The Crestron program finds each Q-SYS control by its exact Named Control text, including capitals and symbols. A Q-SYS design for this room needs every name below.

## Audio levels

| Named Control | Type | Controls | Crestron command | Crestron feedback | Panel function |
|---|---|---|---|---|---|
| `Room1PGMInGain` | Level (Gain) | Program audio level, Gain | COR-001_Output01_VolUp / VolDown / VolDefault_Value | COR-001_Output01_VolBar_Fb | Content Level |
| `Room1PGMInMute` | Button (Mute) | Program audio level, Mute | COR-001_Output01_MuteOff / MuteToggle | COR-001_Output01_Muted_Fb | Content mute |
| `VCMicTxGain` | Level (Gain) | Mic send to conference, Gain | COR-001_Output02_VolUp / VolDown / VolDefault_Value | COR-001_Output02_VolBar_Fb | Not shown on current panel |
| `VCMicTxMute` | Button (Mute) | Mic send to conference, Mute | COR-001_Output02_MuteOff / MuteToggle | COR-001_Output02_Muted_Fb | Not shown on current panel |
| `Room1PCOutGain` | Level (Gain) | Bluetooth audio level, Gain | COR-001_Output03_VolUp / VolDown / VolDefault_Value | COR-001_Output03_VolBar_Fb | Bluetooth Level |
| `Room1PCOutMute` | Button (Mute) | Bluetooth audio level, Mute | COR-001_Output03_MuteOn_Os / MuteOff_Os / MuteToggle | COR-001_Output03_Muted_Fb | Bluetooth mute |
| `Room1PCInGain` | Level (Gain) | Audio from room PC (USB), Gain | COR-001_Input05_VolUp / VolDown / VolDefault_Value | COR-001_Input05_VolBar_Fb | PC In Level |
| `Room1PCInMute` | Button (Mute) | Audio from room PC (USB), Mute | COR-001_Input05_MuteOn_Os / MuteOff_Os / MuteToggle | COR-001_Input05_Muted_Fb | PC In mute |
| `PrivacyMute` | Button (Mute) | Ceiling mic mute before all sends | COR-001_Input03_MuteOn / MuteOff / MuteToggle | COR-001_Input03_Muted, COR-001_Input03_NotMuted | Privacy Mute |
| `Phone1InGain` | Level (Gain) | Softphone receive level, Gain | COR-001_Phone1_In_VolUp / VolDown / VolDefault_Value | COR-001_Phone1_In_VolBar_Fb | Telephone In Level |
| `Phone1InMute` | Button (Mute) | Softphone receive level, Mute | COR-001_Phone1_In_MuteOn / MuteOff / MuteToggle | COR-001_Phone1_In_Muted_Fb | Telephone In mute |
| `Phone1OutputGain` | Level (Gain) | Softphone send level, Gain | COR-001_Phone1_Out_VolUp / VolDown / VolDefault_Value | COR-001_Phone1_Out_VolBar_Fb | Telephone Out Level |
| `Phone1OutputMute` | Button (Mute) | Softphone send level, Mute | COR-001_Phone1_Out_MuteOn / MuteOff / MuteToggle | COR-001_Phone1_Out_Muted_Fb | Telephone Out mute |

## Mic presets

| Named Control | Type | Controls | Crestron command | Crestron feedback | Panel function |
|---|---|---|---|---|---|
| `Preset1` | Trigger + state (one name) | Mic preset 1 snapshot load | COR-001_MicPreset01 (from SysRm01_CeilingPreset1) | COR-001_MicPreset01_Fb | Mic presets, not shown on current panel |
| `Preset2` | Trigger + state (one name) | Mic preset 2 snapshot load | COR-001_MicPreset02 (from SysRm01_CeilingPreset2) | COR-001_MicPreset02_Fb | Mic presets, not shown on current panel |
| `Preset3` | Trigger + state (one name) | Mic preset 3 snapshot load | COR-001_MicPreset03 (from SysRm01_CeilingPreset3) | COR-001_MicPreset03_Fb | Mic presets, not shown on current panel |

## Softphone

| Named Control | Type | Controls | Crestron command | Crestron feedback | Panel function |
|---|---|---|---|---|---|
| `Phone1CallStatusProgress` | String | Softphone, call status text | (feedback only) | COR-001_Phone1_DialStatus$ | Call Status |
| `Phone1CallControlDialString` | String | Softphone, dial string | (module internal) | COR-001_Phone1_NumberDialer$ | Dial number display |
| `Phone1CallStatusRinging(state)` | String | Softphone, ringing state | (feedback only) | COR-001_Phone1_Ringing_FB | Incoming call |
| `Phone1CallStatusOffHook` | String | Softphone, off-hook state | (feedback only) | COR-001_Phone1_IsOffHook_Fb, COR-001_Phone1_IsOnHook_Fb | Hook Status |
| `Phone1DTMFRx` | String | Softphone, received DTMF | (feedback only) | Not used by the room | None |
| `Phone1CallControlDoNotDisturb` | String | Softphone, Do Not Disturb | COR-001_Phone1_DND_toggle | COR-001_Phone1_DND_Fb | DND |
| `Phone1CallControlAutoAnswer` | String | Softphone, Auto Answer | (module internal) | Not used by the room | None |
| `Phone1CallControlConnect` | Trigger | Softphone, Connect | COR-001_Phone1_Dial | (see Ringing/OffHook) | Call |
| `Phone1CallControlDisconnect` | Trigger | Softphone, Disconnect | COR-001_Phone1_HangUpDisconnect | (see Ringing/OffHook) | Hang Up |
| `Phone1CallControlHookFlash` | Trigger | Softphone, Hook Flash | COR-001_Phone1_HookFlash | None | None on screenshots |
| `Phone1PinPad1` | Trigger | Softphone, dial pad 1 | COR-001_Phone1_1_B | None | Keypad 1 |
| `Phone1PinPad2` | Trigger | Softphone, dial pad 2 | COR-001_Phone1_2_B | None | Keypad 2 |
| `Phone1PinPad3` | Trigger | Softphone, dial pad 3 | COR-001_Phone1_3_B | None | Keypad 3 |
| `Phone1PinPad4` | Trigger | Softphone, dial pad 4 | COR-001_Phone1_4_B | None | Keypad 4 |
| `Phone1PinPad5` | Trigger | Softphone, dial pad 5 | COR-001_Phone1_5_B | None | Keypad 5 |
| `Phone1PinPad6` | Trigger | Softphone, dial pad 6 | COR-001_Phone1_6_B | None | Keypad 6 |
| `Phone1PinPad7` | Trigger | Softphone, dial pad 7 | COR-001_Phone1_7_B | None | Keypad 7 |
| `Phone1PinPad8` | Trigger | Softphone, dial pad 8 | COR-001_Phone1_8_B | None | Keypad 8 |
| `Phone1PinPad9` | Trigger | Softphone, dial pad 9 | COR-001_Phone1_9_B | None | Keypad 9 |
| `Phone1PinPad0` | Trigger | Softphone, dial pad 0 | COR-001_Phone1_0_B | None | Keypad 0 |
| `Phone1PinPad*` | Trigger | Softphone, dial pad * | COR-001_Phone1_*_B | None | Keypad * |
| `Phone1PinPad#` | Trigger | Softphone, dial pad # | COR-001_Phone1_#_B | None | Keypad # |
| `Phone1PinPadBackspace` | Trigger | Softphone, backspace | COR-001_Phone1_backspace_B | None | Backspace |
| `Phone1PinPadClear` | Trigger | Softphone, clear number | COR-001_Phone1_Clear | None | Clear |
