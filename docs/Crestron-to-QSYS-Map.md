# Crestron to Q-SYS Map

Named Controls used by the Crestron program. Names are case-sensitive.

## Audio levels

| Q-SYS Named Control | Type | Crestron signal | Function |
|---|---|---|---|
| `Room1PGMInGain` | Level | `COR-001_Output01_Vol` | Content level |
| `Room1PGMInMute` | Mute | `COR-001_Output01_Mute` | Content mute |
| `VCMicTxGain` | Level | `COR-001_Output02_Vol` | Microphone send level |
| `VCMicTxMute` | Mute | `COR-001_Output02_Mute` | Microphone send mute |
| `Room1PCOutGain` | Level | `COR-001_Output03_Vol` | Bluetooth level |
| `Room1PCOutMute` | Mute | `COR-001_Output03_Mute` | Bluetooth mute |
| `Room1PCInGain` | Level | `COR-001_Input05_Vol` | PC level |
| `Room1PCInMute` | Mute | `COR-001_Input05_Mute` | PC mute |
| `PrivacyMute` | Mute | `COR-001_Input03_Mute` | Privacy mute |

## Microphone presets

| Q-SYS Named Control | Type | Crestron signal | Function |
|---|---|---|---|
| `Preset1` | Trigger | `COR-001_MicPreset01` | Preset 1 |
| `Preset2` | Trigger | `COR-001_MicPreset02` | Preset 2 |
| `Preset3` | Trigger | `COR-001_MicPreset03` | Preset 3 |

## Softphone

| Q-SYS Named Control | Type | Crestron signal | Function |
|---|---|---|---|
| `Phone1InGain` | Level | `COR-001_Phone1_In_Vol` | Receive level |
| `Phone1InMute` | Mute | `COR-001_Phone1_In_Mute` | Receive mute |
| `Phone1OutputGain` | Level | `COR-001_Phone1_Out_Vol` | Send level |
| `Phone1OutputMute` | Mute | `COR-001_Phone1_Out_Mute` | Send mute |
| `Phone1CallControlConnect` | Trigger | `COR-001_Phone1_Dial` | Call |
| `Phone1CallControlDisconnect` | Trigger | `COR-001_Phone1_HangUpDisconnect` | Hang up |
| `Phone1CallControlHookFlash` | Trigger | `COR-001_Phone1_HookFlash` | Hook flash |
| `Phone1CallControlDialString` | String | `COR-001_Phone1_NumberDialer$` | Dialed number |
| `Phone1CallControlDoNotDisturb` | String | `COR-001_Phone1_DND_toggle` | Do not disturb |
| `Phone1CallControlAutoAnswer` | String | Module internal | Auto answer |
| `Phone1CallStatusProgress` | String | `COR-001_Phone1_DialStatus$` | Call status |
| `Phone1CallStatusRinging(state)` | String | `COR-001_Phone1_Ringing_FB` | Ringing |
| `Phone1CallStatusOffHook` | String | `COR-001_Phone1_IsOffHook_Fb` | Off hook |
| `Phone1DTMFRx` | String | Module internal | DTMF received |
| `Phone1PinPad0` to `Phone1PinPad9` | Trigger | `COR-001_Phone1_0_B` to `COR-001_Phone1_9_B` | Dial pad digits |
| `Phone1PinPad*` | Trigger | `COR-001_Phone1_*_B` | Dial pad * |
| `Phone1PinPad#` | Trigger | `COR-001_Phone1_#_B` | Dial pad # |
| `Phone1PinPadBackspace` | Trigger | `COR-001_Phone1_backspace_B` | Backspace |
| `Phone1PinPadClear` | Trigger | `COR-001_Phone1_Clear` | Clear |
