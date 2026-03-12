# ZCatalyst Design System — Complete Styles Reference

> Source: ZCatalyst Design System Figma file (`dwQLnT4eJ3zCaOwhk7JXIn`)
> Collections: Mode (Light/Dark), Theme (Default Royal Blue/Purple)
> No paint styles or effect styles — all colors are variable-based.

---

## Table of Contents

- [Text Styles](#text-styles)
- [Color Variables — Mode Collection](#color-variables--mode-collection)
- [Color Variables — Theme Collection](#color-variables--theme-collection)
- [Full Variable Key Reference](#full-variable-key-reference)

---

## Text Styles

26 text styles total. Primary font: **Inter**. Code font: **Roboto Mono**.

| Style Name | Key | Font | Weight | Size | Line Height | Letter Spacing |
|---|---|---|---|---|---|---|
| Service Name | `0960212d4963bc7bb5b8c9f8166310d86cf5ffb2` | Inter | Semi Bold | 16px | 20px | 6% |
| Headlines/H1 | `25a8a1ac56ecfeab817800c7d35a0a854b4c5f17` | Inter | Semi Bold | 40px | Auto | 0 |
| Headlines/H2 | `e3c4e89c4987b83a0de01e874a704698beb2ef79` | Inter | Semi Bold | 32px | Auto | 0 |
| Headlines/H3 | `e51050207ddff0a20d1b1dae80bddbd5b34d4fb2` | Inter | Semi Bold | 24px | 30px | 0 |
| Headlines/H4 | `5773e80e10f3396d8da80218ae0e7799637c42e3` | Inter | Semi Bold | 20px | 24px | 0 |
| Headlines/H5 | `be57224f7a8d40f6fb33855456c324c6fdc58adc` | Inter | Semi Bold | 18px | 22px | 0 |
| Headlines/H6 | `5a352759b8b34ada73a6715ccfe6649bd09b8f9b` | Inter | Semi Bold | 16px | 20px | 0 |
| Body/Subtitle 1 | `51e124811b05455ba4ec2170c2d7d17c606e9850` | Inter | Semi Bold | 14px | 20px | 0 |
| Body/Subtitle 2 | `28ab09c4e20e68276cb6afa9877e62e523225126` | Inter | Semi Bold | 12px | 16px | 0 |
| Body/Subtitle 3 | `d83f1df53b390782a1002c0288f1179081395c9b` | Inter | Semi Bold | 10px | 12px | 0 |
| Body/Body 1 | `dd4a720e10df4ebca0fc96607ae81effb512009e` | Inter | Regular | 14px | 20px | 0 |
| Body/Body 2 | `3ec92fcb0c18950b4de40b4b0481d6411327af2f` | Inter | Regular | 16px | 20px | 0 |
| Body/Body 3 | `540b559794ca7eb23631093b727eddd1d41c14b7` | Inter | Regular | 12px | 16px | 0 |
| Body/Body 4 | `0141e7b3527e7438234bf07bc7279158bf13fc60` | Inter | Regular | 10px | 12px | 0 |
| Body/Body 5 | `e0738f6314e70a6ed9eceeed331fde5c1beccb48` | Inter | Regular | 18px | 22px | 0 |
| Button/Button Lg | `b6c68ad0728e0962f7eff37555924827bfac9083` | Inter | Medium | 16px | 22px | 0 |
| Button/Button Md | `58875ab6a77d036883addb9473f4272de6575482` | Inter | Medium | 14px | 20px | 0 |
| Button/Button Sm | `82dceb66c8f9c997c24907889defda24a24388e6` | Inter | Medium | 14px | 20px | 0 |
| Button/Button XS | `456336493d842efb5ab06a3f70e1f21d91c2a192` | Inter | Medium | 12px | 16px | 0 |
| Input Fields/Label Text | `cb08c2a7d6c5a22cf69315673c6bd2c083572323` | Inter | Semi Bold | 12px | 16px | 0 |
| Input Fields/Default Text | `a3cd3ef68c4573e1188d8ebb2ddf35e78de70421` | Inter | Regular | 14px | 20px | 0 |
| Input Fields/Small Text | `2e582897730de10494722094148a39d67677215b` | Inter | Regular | 14px | 20px | 0 |
| Input Fields/Extra Small Text | `6fd9460657f2f821c73f5db5c0bdff165294b11a` | Inter | Regular | 12px | 16px | 0 |
| Code Text/Code Body | `ea2637050ab70296a1ea8e78fae48b9788150f14` | Roboto Mono | Regular | 12px | 20px | 0 |
| Code Text/Code Subtitle | `9ed93cca872f5a56852b94df2c84472480ea2c02` | Roboto Mono | SemiBold | 12px | 20px | 0 |
| Service Heading/Service Heading | `fa3a3f0ae2cde538a491578bc08f45793bd43fc8` | Inter | Semi Bold | 10px | 12px | 16% |

> **Note:** Text style keys above are full bare keys, ready for `importStyleByKeyAsync(key)`.

---

## Color Variables — Mode Collection

503 total color variables across Mode + Theme collections.
Variables with *(theme)* have no resolved hex — they are **theme aliases** (bound to Theme collection).

> **Note:** Color variable keys below are truncated for readability. For full importable keys, see [Full Variable Key Reference](#full-variable-key-reference) at bottom.

### ACCORDION (14)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Default | `e7a40947c5db…` | → BODY/Text/Static/White | #1A1B1D |
| Background/Hover | `f91de10dff9a…` | #FBFBFB | #1E1F21 |
| Background/Hover 2 | `8cece6799fec…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Background/Active | `5ff3ad66cf66…` | #F4F7FE | #242527 |
| Background/Disable | `cb1eee83ace8…` | #F7F8FB | #242424 |
| Background/Open Bg | `441bcee163ab…` | #FFFFFF | #1A1B1D |
| Background/Icon Bg | `dcf5f5308602…` | #EBEEF6 | #2F3136 |
| Text & Icon/Default | `dd5fbe76e7f4…` | #101F3E | #EEEEEE |
| Text & Icon/Secondary | `60c5b3b0439b…` | #4D618A | #AAAAAA |
| Text & Icon/Disable | `a2706d3524d2…` | #A6B1C9 | #666666 |
| Text & Icon/Secondary Dropdown | `3340e114743e…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text & Icon/Secondary Dropdown Hover | `10d3479d2220…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Border/Default | `c499a100e538…` | #EBEEF6 | #2F3136 |
| Border/Disable | `3cac3c1d2eeb…` | #EFF2FA | #292A2F |

### ATTENTION (25)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Info/Background | `d62baa85304c…` | #E8F5FF | #1B2730 |
| Info/Border | `e2351aef06d3…` | #A6CBEA | #2B4254 |
| Info/Text Primary | `dc4a3525cc1f…` | #101F3E | #EEEEEE |
| Info/Text Secondary | `f8704ce97378…` | #4D618A | #AAAAAA |
| Info/Icon | `0de5021d72e7…` | #101F3E | #EEEEEE |
| Danger/Background | `424e1b41141a…` | #FFEFEF | #2C2123 |
| Danger/Border | `71c0377f3444…` | #EE7979 | #682B2D |
| Danger/Text Primary | `a42bde4fc260…` | #101F3E | #EEEEEE |
| Danger/Text Secondary | `2ba40dc770b3…` | #4D618A | #AAAAAA |
| Danger/Icon | `160a3b21ddf5…` | #101F3E | #EEEEEE |
| Success/Background | `b4d29fdf80ad…` | #EAF7EF | #1C2622 |
| Success/Border | `6757574ac37b…` | #7FD1A0 | #2F4326 |
| Success/Text Primary | `0d29ecb2f606…` | #101F3E | #EEEEEE |
| Success/Text Secondary | `705df56cd9e6…` | #4D618A | #AAAAAA |
| Success/Icon | `6de3412e5594…` | #101F3E | #EEEEEE |
| Warning/Background | `dd1e11ec5d49…` | #FFF3D7 | #27231C |
| Warning/Border | `a8281aaf031c…` | #DAB45F | #493F07 |
| Warning/Text Primary | `d9dcd7c1625c…` | #101F3E | #EEEEEE |
| Warning/Text Secondary | `13472faee698…` | #4D618A | #AAAAAA |
| Warning/Icon | `6a256d7e5a42…` | #101F3E | #EEEEEE |
| Default/Background | `50bc0bb5cc09…` | #F4F7FE | #242527 |
| Default/Border | `7b4ab38e9604…` | #EBEEF6 | #2F3136 |
| Default/Text Primary | `3b0eac94091c…` | #101F3E | #EEEEEE |
| Default/Text Secondary | `a6697465729a…` | #4D618A | #AAAAAA |
| Default/Icon | `9ceb3067d39d…` | #101F3E | #EEEEEE |

### AVATAR (5)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg colors/Default | `601bd9c4b76f…` | #F4F7FE | #242527 |
| Bg colors/Default 2 | `dbfb3659f730…` | #EBEEF6 | #2F3136 |
| Icon/Avatar | `1e94f40c0e84…` | #4D618A | #AAAAAA |
| Borders/Default | `a543012433a3…` | #EBEEF6 | #2F3136 |
| Borders/White | `7f4cb4123419…` | #FFFFFF | #1A1B1D |

### BADGE (22)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Primary | `16089f5b5a3d…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Background/Green | `9ebef43d3e20…` | #29B260 | #3E9F64 |
| Background/Red | `1539e539c598…` | #E22020 | #DE5E60 |
| Background/Pink | `b976cf4d60b8…` | #E417B1 | #DA57B9 |
| Background/Orange | `a7f8a9015ce0…` | #C98E06 | #AE821C |
| Background/Grey | `7896b27087d7…` | #F4F7FE | #242527 |
| Background/Sec- Primary | `26d675e3e49d…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Background/Sec- Red | `ab8a554f6106…` | #FFEFEF | #2C2123 |
| Background/Sec- Pink | `8b775220af01…` | #FFEFFB | #2D202A |
| Background/Sec- Green | `c3db28c42246…` | #EAF7EF | #1C2622 |
| Background/Sec- Orange | `53df569e80c1…` | #FFF3D7 | #27231C |
| Background/Disable | `9ee3e1165938…` | #F7F8FB | #242424 |
| Text/Primary 1 | `df68fc80638c…` | #FFFFFF | #FFFFFF |
| Text/Sec- Primary | `52b4c9d2f698…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text/Sec- Green | `4d7d6044e258…` | #29B260 | #3E9F64 |
| Text/Sec- Red | `67d68f487144…` | #E22020 | #DE5E60 |
| Text/Sec- Pink | `8fc6c16bdfa6…` | #E417B1 | #DA57B9 |
| Text/Sec- Orange | `283e16ca793a…` | #C98E06 | #AE821C |
| Text/Grey | `a17a93961c67…` | #101F3E | #EEEEEE |
| Text/Disable | `533300cf27df…` | #A6B1C9 | #666666 |
| Border - Removed in UI/White | `d118d64a3400…` | #FFFFFF | #1A1B1D |
| Border - Removed in UI/Disabled | `89b2609be766…` | #EFF2FA | #292A2F |

### BODY (16)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Static/Container Bg | `a9b4ed83b5ad…` | #FFFFFF | #1A1B1D |
| Background/Static/Body Bg | `8a73e5eb7acb…` | #EFF2FA | #151516 |
| Border/Static/Border | `dee9b282355c…` | #EBEEF6 | #2F3136 |
| Border/Static/OuterDivider | `71abb67e5096…` | #DDE4F6 | #33373F |
| Text/Static/Primary | `923bd06a923f…` | #101F3E | #EEEEEE |
| Text/Static/Secondary | `cbc2c154ea80…` | #4D618A | #AAAAAA |
| Text/Static/Light | `7a19681638a6…` | #7988A8 | #888888 |
| Text/Static/Disable | `34cb78323c44…` | #A6B1C9 | #666666 |
| Text/Static/Theme | `0e6d1bdb08c3…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text/Static/White | `3b9a2f87cd7c…` | #FFFFFF | #FFFFFF |
| Icons/Static/Primary | `5a84f2ed8100…` | #101F3E | #EEEEEE |
| Icons/Static/Secondary | `4b949396ae94…` | #4D618A | #AAAAAA |
| Icons/Static/Light | `b477aff637a8…` | #7988A8 | #888888 |
| Icons/Static/Disable | `b316d9615de3…` | #A6B1C9 | #666666 |
| Icons/Static/White & Black | `4ff3e20618be…` | #FFFFFF | #1A1B1D |
| Icons/Static/Theme | `ff104a7fb5d3…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |

### BRANDING ICON (2)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Icon Color/Blue | `470ccc11af67…` | #226DB4 | #226DB4 |
| Icon Color/Red | `8fa6ccab91de…` | #E42527 | #E42527 |

### BREADCRUMBS (5)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Hover | `d0087fc1c5be…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Text & Icon/Default | `9158ef260660…` | #4D618A | #AAAAAA |
| Text & Icon/Hover | `26662bd0d528…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text & Icon/Active | `42c876859c78…` | #101F3E | #EEEEEE |
| Text & Icon/Disable | `2a8b7855f0c3…` | #A6B1C9 | #666666 |

### BUTTONS (87)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Fill/Background/Primary | `e2c4d82f0655…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Fill/Background/PrimaryHover | `25c9436b505a…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Fill/Background/PrimaryClick | `78880199cfa7…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Fill/Background/PrimaryDisable | `7f53c83c5553…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Fill/Background/Success | `3185f64a7231…` | #29B260 | #3E9F64 |
| Fill/Background/SuccessHover | `035790398693…` | #218E4D | #3AA564 |
| Fill/Background/SuccessClick | `b31e2caa9141…` | #29B260 | #3E9F64 |
| Fill/Background/SuccessDisable | `8a04ef60cde9…` | #7FD1A0 | #2F4326 |
| Fill/Background/Danger | `ffdc74496d21…` | #E22020 | #DE5E60 |
| Fill/Background/DangerHover | `db9882600c44…` | #B51A1A | #E86E6B |
| Fill/Background/DangerClick | `3a0a14662a28…` | #E22020 | #DE5E60 |
| Fill/Background/DangerDisable | `02b1a06067cc…` | #EE7979 | #682B2D |
| Fill/Text & Icon/Default | `daed13cae3f4…` | #FFFFFF | #FFFFFF |
| Fill/Text & Icon/Hover | `d0843d6d0711…` | #FFFFFF | #FFFFFF |
| Fill/Text & Icon/Click | `e046c87763b9…` | #FFFFFF | #FFFFFF |
| Fill/Text & Icon/Disable | `8dc9aa5b6d3e…` | #E7EEFE | #FFFFFF |
| Fill/Split/Split_Line | `32ef24ba1b3d…` | #FFFFFF | #FFFFFF |
| Outline/Text & Icons/Primary | `67bb93b0273b…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Outline/Text & Icons/PrimaryHover | `c5c9bb2cc2a9…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Outline/Text & Icons/PrimaryClick | `e5a47572ead8…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Outline/Text & Icons/PrimaryDisable | `919c17c20bbb…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Outline/Text & Icons/Success | `6e9e7ff36f35…` | #29B260 | #3E9F64 |
| Outline/Text & Icons/SuccessHover | `f63b5ffa3bc1…` | #218E4D | #3AA564 |
| Outline/Text & Icons/SuccessClick | `41ea272565e7…` | #29B260 | #3E9F64 |
| Outline/Text & Icons/SuccessDisable | `c81ebd719308…` | #7FD1A0 | #2F4326 |
| Outline/Text & Icons/Danger | `42c76df6df6b…` | #E22020 | #DE5E60 |
| Outline/Text & Icons/DangerHover | `f5f4892b4a5a…` | #B51A1A | #E86E6B |
| Outline/Text & Icons/DangerClick | `a1b836582204…` | #E22020 | #DE5E60 |
| Outline/Text & Icons/DangerDisable | `be5a2aa632fb…` | #EE7979 | #682B2D |
| Outline/Borders/Primary | `8b99a5aca59e…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Outline/Borders/PrimaryHover | `aa85eb76fff3…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Outline/Borders/PrimaryClick | `65f542a75639…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Outline/Borders/PrimaryDisable | `eff766176216…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Outline/Borders/Success | `093e6e94b358…` | #29B260 | #3E9F64 |
| Outline/Borders/SuccessHover | `367b780fb238…` | #218E4D | #3AA564 |
| Outline/Borders/SuccessClick | `8bcc1560d200…` | #29B260 | #3E9F64 |
| Outline/Borders/SuccessDisable | `752675a1fee5…` | #7FD1A0 | #2F4326 |
| Outline/Borders/Danger | `870ab37dfb27…` | #E22020 | #DE5E60 |
| Outline/Borders/DangerHover | `6a751b93c4ed…` | #B51A1A | #E86E6B |
| Outline/Borders/DangerClick | `ac00f0b25cdf…` | #E22020 | #DE5E60 |
| Outline/Borders/DangerDisable | `b2d6d88e1249…` | #EE7979 | #682B2D |
| Grey/Backgrounds/Default | `5602e445838d…` | #EBEEF6 | #2F3136 |
| Grey/Backgrounds/Hover | `296e785a3e5d…` | → _Light-Colors/_Primary/Primary-4 | #292A2F |
| Grey/Backgrounds/Click | `10e7d4bd6c37…` | #EBEEF6 | #2F3136 |
| Grey/Backgrounds/Disbale | `67b41273dd73…` | #F7F8FB | #242424 |
| Grey/Text & Icons/Default | `e0fbf1503043…` | #101F3E | #EEEEEE |
| Grey/Text & Icons/Hover | `e260f04641c1…` | #101F3E | #EEEEEE |
| Grey/Text & Icons/Click | `efa1cb232023…` | #101F3E | #EEEEEE |
| Grey/Text & Icons/Disable | `ab64cc5ea3ff…` | #A6B1C9 | #666666 |
| Grey/Borders/Default | `5fd40c21c79e…` | #D6DDEF | #484D58 |
| Grey/Borders/Hover | `650ebe909e9e…` | #D6DDEF | #484D58 |
| Grey/Borders/Click | `3de259e96f4d…` | #D6DDEF | #484D58 |
| Grey/Borders/Disabled | `5a4e6f0d6476…` | #EFF2FA | #292A2F |
| Ghost/Backgrounds/Primary | `4942361d7f20…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Ghost/Backgrounds/Success | `8c7ab5ac43fc…` | #EAF7EF | #1C2622 |
| Ghost/Backgrounds/Danger | `e1ded229a1d8…` | #FFEFEF | #2C2123 |
| Ghost/Text & Icons/PrimaryDefault | `4fcb75f8287b…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Ghost/Text & Icons/PrimaryHover | `4f204f4ac7ae…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Ghost/Text & Icons/PrimaryClick | `0020665c8b03…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Ghost/Text & Icons/PrimaryDisable | `4890e731ab2b…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Ghost/Text & Icons/SuccessDefault | `66d6d00f1b10…` | #29B260 | #3E9F64 |
| Ghost/Text & Icons/SuccessHover | `331cb3515702…` | #218E4D | #3AA564 |
| Ghost/Text & Icons/SuccessClick | `386a5327b352…` | #29B260 | #3E9F64 |
| Ghost/Text & Icons/SuccessDisable | `4223a0365d1f…` | #7FD1A0 | #2F4326 |
| Ghost/Text & Icons/DangerDefault | `db6eeab9e3da…` | #E22020 | #DE5E60 |
| Ghost/Text & Icons/DangerHover | `30f80012aa96…` | #B51A1A | #E86E6B |
| Ghost/Text & Icons/DangerClick | `906d9261513d…` | #E22020 | #DE5E60 |
| Ghost/Text & Icons/DangerDisable | `0d0d8ed0e02e…` | #EE7979 | #682B2D |
| Link/Text & Icon/Default | `62034abc503b…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Link/Text & Icon/Hover | `57183c1b7e2f…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Link/Text & Icon/Click | `0456b52e177f…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Link/Text & Icon/Disable | `1b4ee9083e14…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Outline/Bg/PrimaryHover | `24c01c3bf8ac…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Outline/Bg/SuccessHover | `9fa3619c27be…` | #EAF7EF | #1C2622 |
| Outline/Bg/DangerHover | `51138d0fa076…` | #FFEFEF | #2C2123 |
| Gradient/Text & Icon/Default | `a88688946431…` | #101F3E | #FFFFFF |
| Gradient/Text & Icon/Hover | `9ba9b7fe49c2…` | #101F3E | #FFFFFF |
| Gradient/Text & Icon/Click | `b3048b7f5640…` | #101F3E | #FFFFFF |
| Gradient/Text & Icon/Disable | `0eb818b05e70…` | #A6B1C9 | #FFFFFF |
| Gradient/Bg/Gradient top | `b0404896c72b…` | #FFE1FB | #46224A |
| Gradient/Bg/Gradient bottom | `a3fac0c1a823…` | #C4E7FD | #08293E |
| Gradient/Bg/Gradient top hover | `d21ab45a3109…` | #FFD2F9 | #520D49 |
| Gradient/Bg/Gradient bottom hover | `3133834772b6…` | #B5DDF6 | #2B4B5E |
| Gradient/Bg/Gradient top Click | `4407556520ff…` | #FFE1FB | #46224A |
| Gradient/Bg/Gradient bottom Click | `3bdb4ad76db3…` | #C4E7FD | #08293E |
| Gradient/Bg/Gradient top Disable | `54b59c9aeb6f…` | #FFEFFD | #493546 |
| Gradient/Bg/Gradient bottom Disable | `fa430711322e…` | #DCF2FF | #29333A |

### CARDS (22)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg Default/Primary | `5f31ffd455f6…` | #FFFFFF | #1A1B1D |
| Bg Default/Secondary | `33799101f4d8…` | #FBFBFB | #1E1F21 |
| Bg Default/Teritaroy | `02db6ed6bf18…` | #F4F7FE | #242527 |
| Bg Default/Quaternary | `ba00e89b5c71…` | #EFF2FA | #292A2F |
| Bg Default/Body Bg | `f792049ac254…` | #F7FAFF | #1F2022 |
| Bg Default/Dark Bg | `49bff2d18147…` | #0F2A64 | #1F2022 |
| Bg Hovers/Primary - Hover | `c09f2fa81ddc…` | #FBFBFB | #1E1F21 |
| Bg Hovers/Secondary - Hover | `a141afdd531a…` | #F4F7FE | #242527 |
| Bg Hovers/Teritaroy - Hover | `01984f650dc5…` | #F7FAFF | #1F2022 |
| Bg Hovers/Quaternary - Hover | `ec7cd6cb5bff…` | #F4F7FE | #242527 |
| Bg Hovers/Body Bg - Hover | `21118e62127f…` | #F4F7FE | #242527 |
| Bg Selected/Primary - Selected | `9aae47b19f9b…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Bg Selected/Secondary - Selected | `c17dd566b39a…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Bg Selected/Teritaroy - Selected | `83efef3800b0…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Bg Selected/Quaternary - Selected | `63867f0f5b73…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Bg Selected/Body Bg - Selected | `af02b2b4cbef…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Bg Disabled/Disable | `7d80663ea944…` | #F7F8FB | #242424 |
| Borders/Default | `511f1c301280…` | #EBEEF6 | #2F3136 |
| Borders/Hover | `bacf7f302ae4…` | #DDE4F6 | #33373F |
| Borders/Selected | `fab6eed58da5…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Borders/Disable | `0b1eca41bb43…` | #EFF2FA | #292A2F |
| Borders/White | `b9620d5eae45…` | #FFFFFF | #1A1B1D |

### CAROUSAL (3)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Carosual default | `bbe5c3c7ccbd…` | #A6B1C9 | #666666 |
| Carosual hover | `93b4135fe0f6…` | #4D618A | #AAAAAA |
| Carosual Active | `21b274f1af2f…` | #101F3E | #EEEEEE |

### CHECK, RADIO, TOGGLE (19)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Backgrounds/Default | `b50f3793697d…` | #FFFFFF | #1A1B1D |
| Backgrounds/Hover | `735a4b18a925…` | → _Light-Colors/_Primary/Primary-4 | #292A2F |
| Backgrounds/Disbale | `503bf43f7928…` | #F7F8FB | #242424 |
| Backgrounds/Click | `f345fd3bda8f…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Backgrounds/Click Hover | `c1598d2ccb46…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Backgrounds/Click Disable | `6dd0ce21a5d8…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Inner For Check/White | `f782fce2c988…` | #FFFFFF | #EEEEEE |
| Inner For Toggle/Active | `66144ecdaf00…` | #FFFFFF | #EEEEEE |
| Inner For Radio/White | `707e9ebfd565…` | #FFFFFF | #EEEEEE |
| Inner For Radio/Disable | `2ed99d3d5c6b…` | #E7EEFE | #FFFFFF |
| Inner For Toggle/Active Disable | `16ce9443f70a…` | #E7EEFE | #FFFFFF |
| Inner For Toggle/Default | `f22bb5b116d4…` | #D6DDEF | #484D58 |
| Inner For Toggle/Hover | `4b6ad946463a…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Inner For Toggle/Disabled | `4434ed899077…` | #EBEEF6 | #2F3136 |
| Inner For Check/Disable | `33fbc5b73c3f…` | #E7EEFE | #FFFFFF |
| Borders/Default | `f30e4aa3a3bd…` | #D6DDEF | #484D58 |
| Borders/Hover | `e82732a47acc…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Borders/Disabled | `9f8dbb4b1eed…` | #EFF2FA | #292A2F |
| Borders/Outer Border radio | `46604bfb744d…` | #EBEEF6 | #2F3136 |

### CHIPS (12)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Default | `66043fc5aded…` | #F4F7FE | #242527 |
| Background/Hover | `0ead6b920f4e…` | #F7FAFF | #2F3136 |
| Background/Disable | `56317bc6dfa9…` | #F7F8FB | #242424 |
| Borders/Default | `8d25e25ce197…` | #EBEEF6 | #2F3136 |
| Borders/Hover | `2e772c15d81b…` | #D6DDEF | #484D58 |
| Borders/Disable | `18ef846995bb…` | #EFF2FA | #292A2F |
| Text/Default | `8440e0ab23fd…` | #101F3E | #EEEEEE |
| Text/Hover | `76464ed724fd…` | #101F3E | #EEEEEE |
| Text/Disable | `e5b1cfe520b4…` | #A6B1C9 | #666666 |
| Icons/Active | `e1bd64b98e80…` | #101F3E | #EEEEEE |
| Icons/Hover | `2e08ccf1e7bb…` | #101F3E | #EEEEEE |
| Icons/Disable | `df7392f260ac…` | #A6B1C9 | #666666 |

### CODE BLOCK (3)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg colors/Writer | `c728f4e5b32b…` | #FFFFFF | #1A1B1D |
| Bg colors/Reader | `2307f7211812…` | #F7F8FB | #242527 |
| Borders/Default | `6f99fdb09667…` | #EBEEF6 | #2F3136 |

### DATE PICKER (12)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Datepicker Bg | `be52fe1a691a…` | #FFFFFF | #1A1B1D |
| Background/Number Hover | `cf965cc3ed5c…` | #F4F7FE | #292A2F |
| Background/Number Selected | `ee9b8fb2b55d…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Background/Number Active | `750d81fd1ef4…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Borders/Outer | `9bec599768a7…` | #D6DDEF | #484D58 |
| Borders/Line | `04f1a3a99fce…` | #EBEEF6 | #2F3136 |
| Text/Default | `2f4bfc9d1769…` | #101F3E | #EEEEEE |
| Text/Selected | `3214d0a66d82…` | #FFFFFF | #FFFFFF |
| Text/Active | `d461dbd4816f…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text/Disabled | `9ddea429f6b5…` | #A6B1C9 | #666666 |
| Text/Days | `7cdf0ca0675e…` | #7988A8 | #888888 |
| Text/Headings | `8527bddb8586…` | #101F3E | #EEEEEE |

### FULL PAGE POPUP HEADER (4)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg/Bg | `bef107aa3960…` | #F4F7FE | #292A2F |
| Bg/Bg 2 | `bcfd72e1a8d9…` | #FFFFFF | #1A1B1D |
| Border/Border 1 | `f5c07b6f0289…` | #DDE4F6 | #33373F |
| Text/Text | `29e235fe4e89…` | #101F3E | #EEEEEE |

### GRAPH (5)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Text/Text 1 | `ba4feaa74a43…` | #101F3E | #EEEEEE |
| Text/Text 2 | `80c1424f1192…` | #4D618A | #AAAAAA |
| Text/Text 3 | `a342398d7633…` | #7988A8 | #888888 |
| Lines/X&Y Axis | `b9c1eded6a48…` | #DDE4F6 | #33373F |
| Lines/Line 2 | `cd6ccd0bcd30…` | #EBEEF6 | #2F3136 |

### INPUT_FIELDS (26)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Default | `6f89da5af840…` | #FFFFFF | #1A1B1D |
| Background/Hover | `e0c7191406fd…` | #F7FAFF | #1F2022 |
| Background/Active | `3bfdb15889db…` | #F7FAFF | #1F2022 |
| Background/Disable | `c9bad27be574…` | #F7F8FB | #242424 |
| Background/Error | `f35c691f188c…` | #FFEFEF | #2C2123 |
| Background/Link field Hover | `02ea99f92375…` | #F7FAFF | #1F2022 |
| Borders/Default | `64da02967013…` | #D6DDEF | #484D58 |
| Background/Key value hover | `6fe2e42911f5…` | #F4F7FE | #242527 |
| Borders/Hover | `a0e498137999…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Borders/Active | `c5aeea2b09a0…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Borders/Disable | `c2c17970c911…` | #EFF2FA | #292A2F |
| Borders/Error | `819a284b0c14…` | #EE7979 | #682B2D |
| Text/Place Holder | `e21567fc5e8a…` | #7988A8 | #888888 |
| Text/Active | `1a965815e3b0…` | #101F3E | #EEEEEE |
| Text/Disable | `ce2304800792…` | #A6B1C9 | #666666 |
| Text/Label | `6d7ff5416229…` | #4D618A | #AAAAAA |
| Text/Link field | `47cc0c93b5a1…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text/Link field Hover | `39e7d9414356…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Text/Link Field Active | `1bbb5a756322…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text/Link field disabled | `d320dee7ffdc…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Text/Optional text | `74901cd5f417…` | #7988A8 | #888888 |
| Text/Error Text | `58859395c7f4…` | #E22020 | #DE5E60 |
| Icons/Place Holder | `d19e728d0ab5…` | #7988A8 | #888888 |
| Icons/Active | `885567f6f9b9…` | #101F3E | #EEEEEE |
| Icons/Disable | `307e661335a6…` | #A6B1C9 | #666666 |
| Icons/Label | `582e9d8e2d9d…` | #4D618A | #AAAAAA |

### LINK BOX (12)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Default | `fd3c75cd32e7…` | #F4F7FE | #242527 |
| Background/Hover | `154fed6aba00…` | #EFF2FA | #292A2F |
| Borders/Default | `1abe07c80a3a…` | #EBEEF6 | #2F3136 |
| Borders/Divider | `d57247d806a8…` | #D6DDEF | #484D58 |
| Borders/Hover | `89594295463f…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Text/Label 1 | `84515f65759a…` | #4D618A | #AAAAAA |
| Text/Label 2 | `c66004599043…` | #101F3E | #EEEEEE |
| Text/Main Text | `b45c9d749256…` | #101F3E | #EEEEEE |
| Icons/Label | `9c21cad84263…` | #4D618A | #AAAAAA |
| Icons/Default | `c5b147461232…` | #101F3E | #EEEEEE |
| Icons/Hover | `c2fbe14f0d8f…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Icons/Click | `2807479ad260…` | #101F3E | #EEEEEE |

### LOADER (7)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Content Loader/Primary | `7a3a0cef901d…` | #D6DDEF | #2F3136 |
| Content Loader/Secondary | `014f7d2521c8…` | #F7FAFF | #1F2022 |
| Round Loader/Primary | `a16236e20b8a…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Round Loader/Secondary | `d4dd59c908e5…` | #101F3E | #EEEEEE |
| Round Loader/Teritory | `580efb0db33b…` | #FFFFFF | #1A1B1D |
| Progress Loader/Primary | `c96cf9dc66f8…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Progress Loader/Primary 2 | `cc11ccf9893b…` | #EBEEF6 | #2F3136 |

### MAIN HEADER (5)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg/Bg | `547d945988fb…` | #FFFFFF | #1A1B1D |
| Project Name Logo/Bg | `79286b939d75…` | #EAF7EF | #1C2622 |
| Project Name Logo/Text | `292e51342d60…` | #29B260 | #3E9F64 |
| Border/Border 1 | `ad241d93ce1a…` | #DDE4F6 | #33373F |
| Text/Project text | `32cb2565a994…` | #101F3E | #EEEEEE |

### MENU LIST (14)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Default | `fe46b30affd9…` | #FFFFFF | #1A1B1D |
| Background/List Hover | `664a9eeb7fb8…` | #F4F7FE | #292A2F |
| Background/List Selected | `0a4da841b9b5…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Background/Disable | `574364053a3d…` | #F7F8FB | #242424 |
| Borders/Border | `9ab6624a6fe2…` | #EBEEF6 | #2F3136 |
| Text/Default | `d7ac65ea1b5a…` | #101F3E | #EEEEEE |
| Text/Hover | `2e656314705b…` | #101F3E | #EEEEEE |
| Text/Disable | `5d9b846e23b2…` | #A6B1C9 | #666666 |
| Text/Heading | `d1183de6a945…` | #4D618A | #AAAAAA |
| Text/Light text | `ed36b88552e5…` | #7988A8 | #888888 |
| Icons/Active | `af23c7e39591…` | #101F3E | #EEEEEE |
| Icons/Hover | `2e444e407ff3…` | #101F3E | #EEEEEE |
| Icons/Disable | `305a5690287b…` | #A6B1C9 | #666666 |
| Icons/Check deafult | `2e8cb6a1810c…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |

### OTHER SHADES (28)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Red/Red 1 | `7da69489ce9f…` | #E22020 | #DE5E60 |
| Red/Red 2 | `3ea1defe4bb3…` | #B51A1A | #E86E6B |
| Red/Red 3 | `c736accff700…` | #EE7979 | #682B2D |
| Red/Red 4 | `5dc42d49093c…` | #FFEFEF | #2C2123 |
| Green/Green 1 | `c5b468027686…` | #29B260 | #3E9F64 |
| Theme/Theme 1 | `ce98fc917009…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Theme/Theme 2 | `724edb6d5136…` | → _Light-Colors/_Primary/Primary-2 | → _Dark-Colors/_Primay/Primary-2 |
| Theme/Theme 3 | `0efe8122b8b2…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Theme/Theme 4 | `73e778f18003…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Green/Green 2 | `40849375c329…` | #218E4D | #3AA564 |
| Green/Green 3 | `9cafffd78462…` | #7FD1A0 | #2F4326 |
| Green/Green 4 | `f83e51966951…` | #EAF7EF | #1C2622 |
| Blue/Blue 1 | `95d832925658…` | #2092EF | #4A8EFF |
| Blue/Blue 2 | `c1004017436b…` | #257EC7 | #2E88D1 |
| Blue/Blue 3 | `bda60cd8938d…` | #A6CBEA | #2B4254 |
| Blue/Blue 4 | `2b11eff9da2d…` | #E8F5FF | #1B2730 |
| Pink/Pink 1 | `885bdc052f6b…` | #E417B1 | #DA57B9 |
| Pink/Pink 2 | `8f24525c312d…` | #C51D9B | #CD75B8 |
| Pink/Pink 3 | `b62095d1546e…` | #F8B4E7 | #542F4B |
| Pink/Pink 4 | `3498a4485c80…` | #FFEFFB | #2D202A |
| Orange/Orange 1 | `d1a680043888…` | #C98E06 | #AE821C |
| Orange/Orange 2 | `828eb10cc3e1…` | #A5760C | #A1874B |
| Orange/Orange 3 | `a8c2574fd9a0…` | #DAB45F | #493F07 |
| Orange/Orange 4 | `196dd6808474…` | #FFF3D7 | #27231C |
| Purple/Purple 1 | `09b0d27004fc…` | #6E3D9E | #AD7FE4 |
| Purple/Purple 2 | `d4b9920aceae…` | #7449A4 | #B985F8 |
| Purple/Purple 3 | `da31cc0cd2ae…` | #BDA3DF | #563973 |
| Purple/Purple 4 | `d35755f99574…` | #F1EAFF | #292130 |

### PAGINATION (6)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg/Background | `8f22741a5c3f…` | #FFFFFF | #1A1B1D |
| Bg/Text Primary | `3d687051bfa5…` | #101F3E | #EEEEEE |
| Bg/Text Secondary | `9c27e51dc44c…` | #4D618A | #AAAAAA |
| Bg/Text Teritory | `e22a0b52a671…` | #7988A8 | #888888 |
| Bg/Theme | `c2bf50dd3c9b…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Bg/Divider | `445381ab8550…` | #EBEEF6 | #2F3136 |

### POPUP (4)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Border/Border | `c8300c44a50f…` | #EBEEF6 | #2F3136 |
| Border/OuterBorder | `b489c5076d84…` | #EBEEF6 | #2F3136 |
| Bg/Bg | `25df50a797f0…` | #FFFFFF | #1A1B1D |
| Blur Layer/Bg | `993165bacaa0…` | #101F3E | #000000 |

### PROFILE NAV (19)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Profile Area | `fcae28ef23fe…` | #F4F7FE | #242527 |
| Background/Appearance Light | `e377bd909439…` | #F7F8FB | #F7F8FB |
| Background/Bg Appearance Light | `800ef8dc95a9…` | #FFFFFF | #FFFFFF |
| Background/Line Light 1 | `099b41538332…` | #D6DDEF | #D6DDEF |
| Background/Bg Appearance Light 2 | `eaed157a68e5…` | #EFF2FA | #EFF2FA |
| Background/Line Dark 1 | `a2b463796c04…` | #484D58 | #484D58 |
| Background/Bg Appearance Dark 1 | `1357acb5153a…` | #292A2F | #292A2F |
| Background/Appearance Dark | `01a52ea238c6…` | #242424 | #242424 |
| Background/Bg Appearance Dark | `b2dadeb1c2fb…` | #1A1B1D | #1A1B1D |
| Background/Theme | `786638a078e1…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Background/Theme 2 | `7ff47c93bcc0…` | #E417B1 | #DA57B9 |
| Background/Whilte | `9e5e229638e7…` | #FFFFFF | #FFFFFF |
| Borders/Border | `6a21278d173c…` | #EBEEF6 | #2F3136 |
| Borders/Outer border | `a1675c47acce…` | #D6DDEF | #484D58 |
| Text/Heading | `9cc4b2079e29…` | #101F3E | #EEEEEE |
| Text/Sub Text | `92ab28854c2b…` | #4D618A | #AAAAAA |
| Icons/Light | `729542a5383a…` | #7988A8 | #888888 |
| Icons/Whilte | `24a55028a306…` | #FFFFFF | #FFFFFF |
| Icons/Primary | `98dfb3718420…` | #101F3E | #EEEEEE |

### SERVICE_MENU (9)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/ServiceMenuTop | `35c328fafaf8…` | #0F2A64 | #151516 |
| Background/ServiceMenuBottom | `c0a7d098282e…` | #0A245D | #151516 |
| Background/Icon Bg Default | `cc64bcbb0cf2…` | → _Light-Colors/_Primary/Primary -20% | #242527 |
| Background/Icon Bg Active | `34e1b91449d2…` | → _Light-Colors/_Primary/Primary-4 | #242527 |
| Borders/Side Border | `b8513a014773…` | #4D618A | #33373F |
| Icons/Service icon Default | `6e2dbd99ba5f…` | #FFFFFF | #FFFFFF |
| Text/Sub Heading | `1a241e39e36a…` | #4D618A | #AAAAAA |
| Text/Default | `c029d706a612…` | #FFFFFF | #FFFFFF |
| Text/Active | `174bb7a20438…` | #101F3E | #EEEEEE |

### SHADOWS (2)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Default | `9087ddd60b49…` | #EFF2FA | #292A2F |
| Background/With Opacity | `815cca3b157d…` | #EFF2FA | #292A2F |

### SIDE MENU (10)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Sidemenu Bg | `eee914c636e1…` | → BODY/Text/Static/White | #1A1B1D |
| Background/Menu Hover | `ce2bab60ba07…` | #F4F7FE | #292A2F |
| Background/Menu Active | `143b5caf6af6…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Text & Icon/Default | `0c9c338f9336…` | #101F3E | #AAAAAA |
| Text & Icon/Hover | `26e694943442…` | → _Light-Colors/_Primary/Primary-1 | #EEEEEE |
| Text & Icon/Active | `a603977717f6…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text & Icon/Disable | `fc1b2400830a…` | #A6B1C9 | #666666 |
| Text & Icon/Sub Heading | `f5af51bde7bd…` | #7988A8 | #666666 |
| Text & Icon/Service Name | `5fbe48b7ee43…` | #101F3E | #EEEEEE |
| Borders/Default | `f2a52ab89f98…` | #DDE4F6 | #33373F |

### STEPPER (17)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg colors/Default | `5bcda7175a9d…` | #F4F7FE | #242527 |
| Bg colors/Active | `b3926f9d4984…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Bg colors/Completed | `3683a86ee478…` | #29B260 | #3E9F64 |
| Bg colors/Disable | `30a4113b98e8…` | #F7F8FB | #242424 |
| Text/Default | `78a33196e051…` | #4D618A | #AAAAAA |
| Text/Sub Text | `5fde63884a39…` | #4D618A | #AAAAAA |
| Text/Active | `a80bf1f7f4dd…` | #101F3E | #EEEEEE |
| Text/Completed | `150c79ac6d7f…` | #101F3E | #EEEEEE |
| Text/Disable | `a048c6a61180…` | #A6B1C9 | #666666 |
| Text/Numbers | `ba20773e04ae…` | #FFFFFF | #FFFFFF |
| Divider/Default | `f01deeabc27d…` | #D6DDEF | #484D58 |
| Divider/Active | `026886d4cb92…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Divider/Completed | `6c39c4da90c9…` | #3E9F64 | #3E9F64 |
| Divider/Disable | `8e217d8f9402…` | #EFF2FA | #292A2F |
| Borders/Default | `4e7475919a40…` | #D6DDEF | #484D58 |
| Borders/Active | `67393a8a35cd…` | #FFFFFF | #FFFFFF |
| Borders/Disable | `ebe6232bc15c…` | #FFFFFF | #FFFFFF |

### SUB HEADERS (3)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Bg/Bg | `d01fc49e6374…` | #FFFFFF | #1A1B1D |
| Border/Border 1 | `189f79e777bc…` | #DDE4F6 | #33373F |
| Text/Border 1 | `4cc977306cf9…` | #101F3E | #EEEEEE |

### TABLE (18)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Text/Primary | `20b8e89471a8…` | #101F3E | #EEEEEE |
| Text/Secondary | `7f68959b4e43…` | #4D618A | #AAAAAA |
| Text/Light | `e7864ff431bc…` | #7988A8 | #888888 |
| Text/Disable | `7a9b38e510f0…` | #A6B1C9 | #666666 |
| Icons/Primary | `886312b190a3…` | #101F3E | #EEEEEE |
| Icons/Secondary | `7d99de0c3244…` | #4D618A | #AAAAAA |
| Icons/Light | `ce512152afe0…` | #7988A8 | #888888 |
| Icons/Disable | `a53460ff6102…` | #A6B1C9 | #666666 |
| Borders/Default | `12f8dd08bef8…` | #EBEEF6 | #2F3136 |
| Background/Row_Bg | `6d8230c98338…` | #FFFFFF | #1A1B1D |
| Background/Header_Bg | `6c29cc20c8ae…` | #F7F8FB | #1E1F21 |
| Background/Row_Hover_Bg | `955876596ab4…` | #F4F7FE | #242527 |
| Background/Row_Selected_Bg | `0b5550646efc…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Background/Row_Disabled_Bg | `d476e9059e1f…` | #F7F8FB | #242424 |
| Three_Dot/Icon | `8531d854dde0…` | #101F3E | #EEEEEE |
| Three_Dot/Icon_Bg | `41f973b38a50…` | #F7F8FB | #242424 |
| Three_Dot/Icon_Bg_Hover | `9f074f54532b…` | #EBEEF6 | #2F3136 |
| Three_Dot/Icon_Bg_Active | `643194cf8449…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |

### TABS (28)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Primary/Background/Hover | `965755385dab…` | → _Light-Colors/_Primary/Primary-4 | → _Dark-Colors/_Primay/Primary-4 |
| Primary/Borders/Default | `f4a1f532c0fa…` | #DDE4F6 | #33373F |
| Primary/Borders/Hover | `74965b821948…` | → _Light-Colors/_Primary/Primary-3 | → _Dark-Colors/_Primay/Primary-3 |
| Primary/Borders/Active | `30a603846777…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Primary/Borders/Disable | `8a2105ec3c9d…` | #EFF2FA | #292A2F |
| Primary/Text & Icon/Default | `f5fc0c507baf…` | #4D618A | #AAAAAA |
| Primary/Text & Icon/Hover | `d2e15c37a44b…` | #101F3E | #EEEEEE |
| Primary/Text & Icon/Active | `ca6d55766091…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Primary/Text & Icon/Disable | `b094ebbe0652…` | #A6B1C9 | #666666 |
| Primary/Background/Disable | `d79dd62c94cf…` | #F7F8FB | #242424 |
| Secondary/Background/Active | `78b052b6a340…` | #FFFFFF | #1F2022 |
| Secondary/Background/Hover | `e42420a1f462…` | #FFFFFF | #292A2F |
| Secondary/Text & Icon/Default | `4fb70763520a…` | #4D618A | #AAAAAA |
| Secondary/Text & Icon/Hover | `95e7577e6b2d…` | #101F3E | #EEEEEE |
| Secondary/Text & Icon/Active | `f3a15a84ceb0…` | → _Light-Colors/_Primary/Primary-1 | #EEEEEE |
| Secondary/Text & Icon/Disable | `25ab611fdc26…` | #A6B1C9 | #666666 |
| Secondary/Background/Disable | `3c5ce580839b…` | #F7F8FB | #242424 |
| Secondary/Background/BG Default | `7fec9035d199…` | #EFF2FA | #33373F |
| Secondary/Border/Default | `aa5903f06837…` | #DDE4F6 | #33373F |
| Code Tab/Background/Active | `250e8bd2d697…` | #FFFFFF | #1F2022 |
| Code Tab/Background/Hover | `bbf8fd0eaf02…` | #FFFFFF | #292A2F |
| Code Tab/Text & Icon/Default | `c95916476958…` | #4D618A | #AAAAAA |
| Code Tab/Text & Icon/Hover | `9ba58d097823…` | #101F3E | #EEEEEE |
| Code Tab/Text & Icon/Active | `76bddc950f85…` | → _Light-Colors/_Primary/Primary-1 | #EEEEEE |
| Code Tab/Text & Icon/Disable | `7a098792c1d9…` | #A6B1C9 | #666666 |
| Code Tab/Background/Disable | `d8dc0b0076a3…` | #F7F8FB | #242424 |
| Code Tab/Background/BG Default | `fcb7968552cd…` | #EFF2FA | #292A2F |
| Code Tab/Border/Default | `75b5e93945da…` | #DDE4F6 | #33373F |

### TIMELINE (11)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/Green | `056da3a853ef…` | #EAF7EF | #1C2622 |
| Background/Green Dot | `162e9615f8b2…` | #29B260 | #3E9F64 |
| Background/Orange | `d2e4a3fc41d2…` | #FFF3D7 | #27231C |
| Background/Orange dot | `176c3d86f51c…` | #C98E06 | #AE821C |
| Background/Blue | `2c41a0f65cdf…` | #E8F5FF | #1B2730 |
| Background/Blue Dot | `c8cc67edc1c7…` | #2092EF | #4A8EFF |
| Background/Red | `49c52d0f4462…` | #FFEFEF | #2C2123 |
| Background/Red Dot | `ddde92de0050…` | #E22020 | #DE5E60 |
| Background/Grey | `1360bee496b2…` | #EBEEF6 | #2F3136 |
| Background/Grey Dot | `312d4c73cbed…` | #4D618A | #AAAAAA |
| Line/Default | `315da92de675…` | #D6DDEF | #484D58 |

### TOAST (8)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Default/Background | `7556cc809c5f…` | #FFFFFF | #1A1B1D |
| Default/Border | `f40ad4bda3e5…` | #EBEEF6 | #2F3136 |
| Default/Icon, Line Success | `1169fac02adc…` | #29B260 | #3E9F64 |
| Default/Icon, Line Danger | `4a4203f61a7c…` | #E22020 | #DE5E60 |
| Default/Icon, Line Info | `5b95ca5839f2…` | #2092EF | #4A8EFF |
| Default/Icon, Line Warning | `87144bd21f1d…` | #C98E06 | #AE821C |
| Default/Text Primary | `54b626c9b5bd…` | #101F3E | #EEEEEE |
| Default/Text Secondary | `c5dbd56e8b33…` | #4D618A | #AAAAAA |

### TOOLTIP (4)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Static/Background | `825c222acb6a…` | #101F3E | #2F3136 |
| Static/Text Primary | `81a642904fcc…` | #FFFFFF | #FFFFFF |
| Static/Border | `50bdb8009e65…` | #EBEEF6 | #484D58 |
| Static/Text Secondary | `cebe62e055c6…` | #4D618A | #AAAAAA |

### TOUR (6)

| Variable | Key | Light | Dark |
|---|---|---|---|
| Background/default | `e8b7b291141d…` | #FFFFFF | #1A1B1D |
| Background/Blink bg | `0f91ea3de06f…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Borders/Outer | `a5edfb9be662…` | #EBEEF6 | #2F3136 |
| Borders/Blink Border | `60cde610bc97…` | → _Light-Colors/_Primary/Primary-1 | → _Dark-Colors/_Primay/Primary-1 |
| Text/Heading | `f099aa0ba979…` | #101F3E | #EEEEEE |
| Text/Sub Text | `67c64a0f62ad…` | #4D618A | #AAAAAA |

---

## Color Variables — Theme Collection

10 theme variables. Modes: **Default Royal Blue** / **Purple**.

| Variable | Key | Default Royal Blue | Purple |
|---|---|---|---|
| Default - RoyalBlue/L Primary | `0017910cc3ec…` | #2A65F0 | #6E3D9E |
| Default - RoyalBlue/L Primary 2 | `702c6244c327…` | #0755F2 | #7449A4 |
| Default - RoyalBlue/LPrimary 3 | `50796799a532…` | #7DA2FB | #BDA3DF |
| Default - RoyalBlue/L Primary 4 | `d4a1d439b9fa…` | #E7EEFE | #E9DEFF |
| Default - RoyalBlue/L Primary 20% | `7b68557c4811…` | #2A65F0 | #6E3D9E |
| Default - RoyalBlue/D Primary | `111e066b869b…` | #458BFF | #AD7FE4 |
| Default - RoyalBlue/D Primary 2 | `62e1772fb2f4…` | #5A97FB | #B985F8 |
| Default - RoyalBlue/D Primary 3 | `44bc818f88de…` | #355A8D | #563973 |
| Default - RoyalBlue/D Primary 4 | `98ea108edb80…` | #1A273D | #2B1B3A |
| Default - RoyalBlue/D Primary 20% | `855a0973d201…` | #2074FF | #582B84 |

---

## Full Variable Key Reference

For use with `figma.variables.importVariableByKeyAsync(key)`.

<details>
<summary>Click to expand all 503 variable keys</summary>

| Variable Name | Collection | Full Key |
|---|---|---|
| BODY/Background/Static/Container Bg | Mode | `a9b4ed83b5ad5b5fe00bc4e56a141e92ad8dae02` |
| BODY/Background/Static/Body Bg | Mode | `8a73e5eb7acb073d9207bddf09a19287115b4cfd` |
| BODY/Border/Static/Border | Mode | `dee9b282355cc41a5865a29cc8fc48d6b80484ec` |
| BODY/Border/Static/OuterDivider | Mode | `71abb67e509670e8bc2a18aecd730ae64a7eb0d7` |
| BODY/Text/Static/Primary | Mode | `923bd06a923fee3c9811bed53c2e1023d667e99f` |
| BODY/Text/Static/Secondary | Mode | `cbc2c154ea80793b1cc0707f853d43e59a96cf04` |
| BODY/Text/Static/Light | Mode | `7a19681638a68e906bddd75586271d7836762473` |
| BODY/Text/Static/Disable | Mode | `34cb78323c4482bb9ddd65aa567b609282734f7b` |
| BODY/Text/Static/Theme | Mode | `0e6d1bdb08c318e876eafd4be5915c3266191fae` |
| BODY/Text/Static/White | Mode | `3b9a2f87cd7cb2db22e52bba6c1fe2ba97a31b0e` |
| BODY/Icons/Static/Primary | Mode | `5a84f2ed810016b3efb87e427e84cc49562309fa` |
| BODY/Icons/Static/Secondary | Mode | `4b949396ae9456a5e3e8c5f211b2904a88ac33c0` |
| BODY/Icons/Static/Light | Mode | `b477aff637a8016f87deb55b8d1aa6a43b0f5e6e` |
| BODY/Icons/Static/Disable | Mode | `b316d9615de355d47faaf643baad606d3bc7efe5` |
| BODY/Icons/Static/White & Black | Mode | `4ff3e20618be8f9b55ba4a4449f8c6355442adc5` |
| BODY/Icons/Static/Theme | Mode | `ff104a7fb5d301d5943d7172ed0beef76aa1fece` |
| CARDS/Bg Default/Primary | Mode | `5f31ffd455f693c79bb692d089dc99c045508bde` |
| CARDS/Bg Default/Secondary | Mode | `33799101f4d87567229f94849487afeffa6750c0` |
| CARDS/Bg Default/Teritaroy | Mode | `02db6ed6bf18105b51bf83233ba8e4e8a74cd7ac` |
| CARDS/Bg Default/Quaternary | Mode | `ba00e89b5c711bf24e1968fa24271ef59f95c4e2` |
| CARDS/Bg Default/Body Bg | Mode | `f792049ac254d1470ff270909b54301a96b90065` |
| CARDS/Bg Default/Dark Bg | Mode | `49bff2d18147a84c6c9fd317811e189462cf81f6` |
| CARDS/Bg Hovers/Primary - Hover | Mode | `c09f2fa81ddc2c98fd57595ba69e2d302ed6e47a` |
| CARDS/Bg Hovers/Secondary - Hover | Mode | `a141afdd531a80e585c133bfe83117de6c48e855` |
| CARDS/Bg Hovers/Teritaroy - Hover | Mode | `01984f650dc585ed77c9633bf51f50b2dc7cad85` |
| CARDS/Bg Hovers/Quaternary - Hover | Mode | `ec7cd6cb5bffe4aa4dc7b30b1ffc1c083f8cd825` |
| CARDS/Bg Hovers/Body Bg - Hover | Mode | `21118e62127fceddd728e56fe085333616cc959c` |
| CARDS/Bg Selected/Primary - Selected | Mode | `9aae47b19f9b90c4b846352692b127c5b78fb0fd` |
| CARDS/Bg Selected/Secondary - Selected | Mode | `c17dd566b39a1dab068622fac7f00d786df38c25` |
| CARDS/Bg Selected/Teritaroy - Selected | Mode | `83efef3800b083700e66543494967dcd6444d8d3` |
| CARDS/Bg Selected/Quaternary - Selected | Mode | `63867f0f5b73abd04359cfbd3a9f44e57b2504b8` |
| CARDS/Bg Selected/Body Bg - Selected | Mode | `af02b2b4cbef026aa7600c7197915ba50af66571` |
| CARDS/Bg Disabled/Disable | Mode | `7d80663ea944d0cc0d90753736ad8e88362f408c` |
| CARDS/Borders/Default | Mode | `511f1c30128041f0816ec4025aed7cc050584519` |
| CARDS/Borders/Hover | Mode | `bacf7f302ae4d0159192d51a810e5912e7f20d89` |
| CARDS/Borders/Selected | Mode | `fab6eed58da56edd8dc4647b8ad971892fcaf4d0` |
| CARDS/Borders/Disable | Mode | `0b1eca41bb434fb789473e378b2a1a661bfe6a2d` |
| CARDS/Borders/White | Mode | `b9620d5eae45f0e705bf594024073e673959dcc2` |
| SHADOWS/Background/Default | Mode | `9087ddd60b49acf3baa5d2752af9ed43da350800` |
| SHADOWS/Background/With Opacity | Mode | `815cca3b157d974378255bdc699c951143f3a44a` |
| OTHER SHADES/Red/Red 1 | Mode | `7da69489ce9f98f8ddfb85a66724a1d6d74fb409` |
| OTHER SHADES/Red/Red 2 | Mode | `3ea1defe4bb35e67993ccbe09eef060b854e63eb` |
| OTHER SHADES/Red/Red 3 | Mode | `c736accff700057c5ae9d7032b31640703e4983c` |
| OTHER SHADES/Red/Red 4 | Mode | `5dc42d49093cedf272fbcf74f6da1009406fd2b8` |
| BUTTONS/Fill/Background/Primary | Mode | `e2c4d82f065511a5bcd65b9fbf4ccf092d720b85` |
| BUTTONS/Fill/Background/PrimaryHover | Mode | `25c9436b505a6681d77685dae8ead0372ac99851` |
| BUTTONS/Fill/Background/PrimaryClick | Mode | `78880199cfa708b2888eceafc10e993d730fcce0` |
| BUTTONS/Fill/Background/PrimaryDisable | Mode | `7f53c83c5553b814b1d77f610cda3679400afa6e` |
| BUTTONS/Fill/Background/Success | Mode | `3185f64a7231a574e61ceed9e06d9c093142c257` |
| BUTTONS/Fill/Background/SuccessHover | Mode | `0357903986937dc96bdfc99d49ecc7547b875a89` |
| BUTTONS/Fill/Background/SuccessClick | Mode | `b31e2caa9141235c546da79d35138d9caaeb704a` |
| BUTTONS/Fill/Background/SuccessDisable | Mode | `8a04ef60cde942d1af449f15942bf2f522fd45d5` |
| BUTTONS/Fill/Background/Danger | Mode | `ffdc74496d2136764e64ce9278626afd2feef1d2` |
| BUTTONS/Fill/Background/DangerHover | Mode | `db9882600c4420618fc3e67398a5f9b0291a56a7` |
| BUTTONS/Fill/Background/DangerClick | Mode | `3a0a14662a28b0717750ec9f28f3eaa3e602f6d2` |
| BUTTONS/Fill/Background/DangerDisable | Mode | `02b1a06067cc36bab0afdad0b19f17a569251d80` |
| BUTTONS/Fill/Text & Icon/Default | Mode | `daed13cae3f4cf2593ed75e6ff3cff533939f1cd` |
| BUTTONS/Fill/Text & Icon/Hover | Mode | `d0843d6d0711a3eabc83be0f4b2ce1d16283020b` |
| BUTTONS/Fill/Text & Icon/Click | Mode | `e046c87763b9504ebfc38ec5c0d8fca8432998cd` |
| BUTTONS/Fill/Text & Icon/Disable | Mode | `8dc9aa5b6d3e029917e6051d9c45be4fd67ec2c8` |
| BUTTONS/Fill/Split/Split_Line | Mode | `32ef24ba1b3d426859cffe71a214967208bc12a5` |
| BUTTONS/Outline/Text & Icons/Primary | Mode | `67bb93b0273bd0f77b10496d82c3c109b9bbef3d` |
| BUTTONS/Outline/Text & Icons/PrimaryHover | Mode | `c5c9bb2cc2a9aaeb11c794a3b2339ce4777bd44a` |
| BUTTONS/Outline/Text & Icons/PrimaryClick | Mode | `e5a47572ead8a703bb6654aace9fbccb7e92101f` |
| BUTTONS/Outline/Text & Icons/PrimaryDisable | Mode | `919c17c20bbb5f2a799ee7c5d2807a65bf8324cc` |
| BUTTONS/Outline/Text & Icons/Success | Mode | `6e9e7ff36f350086d23fb0e573d143661c8a36b4` |
| BUTTONS/Outline/Text & Icons/SuccessHover | Mode | `f63b5ffa3bc1fac70b9ed5f62f79e6129933f404` |
| BUTTONS/Outline/Text & Icons/SuccessClick | Mode | `41ea272565e767f1ea7498cf8dda4f050c600b35` |
| BUTTONS/Outline/Text & Icons/SuccessDisable | Mode | `c81ebd7193084c17f3fe5c20deac1b344b58deba` |
| BUTTONS/Outline/Text & Icons/Danger | Mode | `42c76df6df6ba55246ea2949bc031cee5a554187` |
| BUTTONS/Outline/Text & Icons/DangerHover | Mode | `f5f4892b4a5a83628ec24cb80fb995f9b06c662f` |
| BUTTONS/Outline/Text & Icons/DangerClick | Mode | `a1b8365822042b7a4fa24d5a41e228cc1a70dc26` |
| BUTTONS/Outline/Text & Icons/DangerDisable | Mode | `be5a2aa632fb5553b05f43746a9dbce2f1830653` |
| BUTTONS/Outline/Borders/Primary | Mode | `8b99a5aca59e2a8e26df7e43fd20c31fec39bebd` |
| BUTTONS/Outline/Borders/PrimaryHover | Mode | `aa85eb76fff3a485de16ff39c8685d4dc3f60e05` |
| BUTTONS/Outline/Borders/PrimaryClick | Mode | `65f542a7563959a0267edcbc43885d099d29b0ce` |
| BUTTONS/Outline/Borders/PrimaryDisable | Mode | `eff7661762168f786a2257002ecab3cc513487dc` |
| BUTTONS/Outline/Borders/Success | Mode | `093e6e94b358ab95f901d5429a735d8d91e8b0df` |
| BUTTONS/Outline/Borders/SuccessHover | Mode | `367b780fb238c2f2c4cbbd825b37d92f3261e3dc` |
| BUTTONS/Outline/Borders/SuccessClick | Mode | `8bcc1560d2003cfce8e7dc4e9bcd26632d5f2258` |
| BUTTONS/Outline/Borders/SuccessDisable | Mode | `752675a1fee5ce9bd0b03eaa3c615e51c33854a5` |
| BUTTONS/Outline/Borders/Danger | Mode | `870ab37dfb27a8801dd207f84a9e2fcad2c42283` |
| BUTTONS/Outline/Borders/DangerHover | Mode | `6a751b93c4eda4aec0075bc6af619c9e3aeb6b8f` |
| BUTTONS/Outline/Borders/DangerClick | Mode | `ac00f0b25cdfe0c539d766054d844e55c3db6c0a` |
| BUTTONS/Outline/Borders/DangerDisable | Mode | `b2d6d88e124964c6ee03e55f6e48d7efb5c448b6` |
| BUTTONS/Grey/Backgrounds/Default | Mode | `5602e445838dbb7c05f9a52b9cd3ec7b6c954d8b` |
| BUTTONS/Grey/Backgrounds/Hover | Mode | `296e785a3e5de58adad848cf3ef7cc0d503b7619` |
| BUTTONS/Grey/Backgrounds/Click | Mode | `10e7d4bd6c378e112476416f0cf83d2b6a250fb5` |
| BUTTONS/Grey/Backgrounds/Disbale | Mode | `67b41273dd73ef185aab49d396a7d30b8baab6d3` |
| BUTTONS/Grey/Text & Icons/Default | Mode | `e0fbf1503043819eae37a8e4beaa201dbee53f87` |
| BUTTONS/Grey/Text & Icons/Hover | Mode | `e260f04641c123e654ae36a01459b4886dd6b2a9` |
| BUTTONS/Grey/Text & Icons/Click | Mode | `efa1cb232023f164b819834956299e66b73bcfc7` |
| BUTTONS/Grey/Text & Icons/Disable | Mode | `ab64cc5ea3fff2f81b01c473a6f50fa9f6eb7ffb` |
| BUTTONS/Grey/Borders/Default | Mode | `5fd40c21c79e0e27e0444f03db6cd8ea26278691` |
| BUTTONS/Grey/Borders/Hover | Mode | `650ebe909e9e8c79d324f8cda7f2e653c7f96bb3` |
| BUTTONS/Grey/Borders/Click | Mode | `3de259e96f4d1fe29b8e325f25c372ed0747205f` |
| BUTTONS/Grey/Borders/Disabled | Mode | `5a4e6f0d64765a010a37c4ccb8762258b022f260` |
| BUTTONS/Ghost/Backgrounds/Primary | Mode | `4942361d7f20169e3b4b6638fd433d656cf107bc` |
| BUTTONS/Ghost/Backgrounds/Success | Mode | `8c7ab5ac43fc2ed026fc2baad6ba2f4ba62afae5` |
| BUTTONS/Ghost/Backgrounds/Danger | Mode | `e1ded229a1d8be95f061ae8aa001274a5ddb3c04` |
| BUTTONS/Ghost/Text & Icons/PrimaryDefault | Mode | `4fcb75f8287ba8df9363db69b3b94c4d7dc869dd` |
| BUTTONS/Ghost/Text & Icons/PrimaryHover | Mode | `4f204f4ac7ae54401640ab7f30d264535c05465e` |
| BUTTONS/Ghost/Text & Icons/PrimaryClick | Mode | `0020665c8b03016dd17777b365042a4b2d811419` |
| BUTTONS/Ghost/Text & Icons/PrimaryDisable | Mode | `4890e731ab2b184ba07f08fce1634025d924537e` |
| BUTTONS/Ghost/Text & Icons/SuccessDefault | Mode | `66d6d00f1b10e65392cb75faa0f8e3276ce62838` |
| BUTTONS/Ghost/Text & Icons/SuccessHover | Mode | `331cb351570246f36b5e51aed18e3d9fd3c219a5` |
| BUTTONS/Ghost/Text & Icons/SuccessClick | Mode | `386a5327b3525f6642559fd892dc0b2e1e17020a` |
| BUTTONS/Ghost/Text & Icons/SuccessDisable | Mode | `4223a0365d1f6a68bb267a8320f80af653b30d0f` |
| BUTTONS/Ghost/Text & Icons/DangerDefault | Mode | `db6eeab9e3da9bb3dab5997986efc79b592f6b1b` |
| BUTTONS/Ghost/Text & Icons/DangerHover | Mode | `30f80012aa967be1b0703ec22a81e71e63529135` |
| BUTTONS/Ghost/Text & Icons/DangerClick | Mode | `906d9261513da6417b40ae6398523e11e98b81e3` |
| BUTTONS/Ghost/Text & Icons/DangerDisable | Mode | `0d0d8ed0e02eaf2311b35ecd1a179ef05bdde680` |
| BUTTONS/Link/Text & Icon/Default | Mode | `62034abc503b940fba9beb8abd1e355e305a7e74` |
| BUTTONS/Link/Text & Icon/Hover | Mode | `57183c1b7e2f2b4183ac12f10e5ac7cd00a2e8f7` |
| BUTTONS/Link/Text & Icon/Click | Mode | `0456b52e177f52bb6c6066f329b5c28849b5cc0c` |
| BUTTONS/Link/Text & Icon/Disable | Mode | `1b4ee9083e141c833615f003c8a5bcd55a880925` |
| TABLE/Text/Primary | Mode | `20b8e89471a8942a5f9d7be6d7b991dcf3f874d0` |
| TABLE/Text/Secondary | Mode | `7f68959b4e43f477ca3d708b4c70760365ec8a38` |
| TABLE/Text/Light | Mode | `e7864ff431bc05184cf3ae0559a055556cb1325b` |
| TABLE/Text/Disable | Mode | `7a9b38e510f0f3265bfe0480521fcc392444b495` |
| TABLE/Icons/Primary | Mode | `886312b190a3856a721c6010b3ccb080382301be` |
| TABLE/Icons/Secondary | Mode | `7d99de0c3244614dd5997d01ccf3ace18295a047` |
| TABLE/Icons/Light | Mode | `ce512152afe0ed67ae62c14d9d1d18f5d53e31b5` |
| TABLE/Icons/Disable | Mode | `a53460ff6102097c0c5430a1e465718b283ad675` |
| TABLE/Borders/Default | Mode | `12f8dd08bef851c584bb7c98e7dd08531a8b7fdc` |
| TABLE/Background/Row_Bg | Mode | `6d8230c98338cb82637668ac9aaa8d5de38fe394` |
| TABLE/Background/Header_Bg | Mode | `6c29cc20c8aeced013d0864c4dcce61571621a38` |
| TABLE/Background/Row_Hover_Bg | Mode | `955876596ab47d203c76963f9ab187f598c824e7` |
| TABLE/Background/Row_Selected_Bg | Mode | `0b5550646efc37398b96251e66ea072a62c24411` |
| TABLE/Background/Row_Disabled_Bg | Mode | `d476e9059e1ff3ddb65bcbe95ef4fe328d458954` |
| TABLE/Three_Dot/Icon | Mode | `8531d854dde0b8a17cff0b2ad6861cd92df45d52` |
| TABLE/Three_Dot/Icon_Bg | Mode | `41f973b38a500bd2137f5c36fadb845088b71d51` |
| TABLE/Three_Dot/Icon_Bg_Hover | Mode | `9f074f54532b2b54754d0920077d6efcae05db10` |
| TABLE/Three_Dot/Icon_Bg_Active | Mode | `643194cf8449a0176a9874613586f34cdb089e24` |
| SERVICE_MENU/Background/ServiceMenuTop | Mode | `35c328fafaf892805387b4368bcb2b4cc4b73de6` |
| SERVICE_MENU/Background/ServiceMenuBottom | Mode | `c0a7d098282e0037fc87bb4058ee6950bbbd1b9e` |
| SERVICE_MENU/Background/Icon Bg Default | Mode | `cc64bcbb0cf249b92999cee15536f730c9732a65` |
| SERVICE_MENU/Background/Icon Bg Active | Mode | `34e1b91449d29fc60106bac6dd3dc85bd80b2c97` |
| INPUT_FIELDS/Background/Default | Mode | `6f89da5af8400de875db1fde0f033af05a49164b` |
| INPUT_FIELDS/Background/Hover | Mode | `e0c7191406fd2b23b75ec992798a11346b24aeae` |
| INPUT_FIELDS/Background/Active | Mode | `3bfdb15889dba404243c06ce5581d99abef87344` |
| INPUT_FIELDS/Background/Disable | Mode | `c9bad27be5743a910b39e560786d9f1fdaa0cf33` |
| INPUT_FIELDS/Background/Error | Mode | `f35c691f188c547f979a0fd1ee88d1f63fc32be9` |
| INPUT_FIELDS/Background/Link field Hover | Mode | `02ea99f92375b258154a3690d3449c0633f31d40` |
| INPUT_FIELDS/Borders/Default | Mode | `64da029670139a3c554e2c6432665e6adf1b737a` |
| INPUT_FIELDS/Background/Key value hover | Mode | `6fe2e42911f5b02abaa1c5a68f80f3d0d95bf5a3` |
| INPUT_FIELDS/Borders/Hover | Mode | `a0e4981379998e2a3bae8361c0661034383010c8` |
| INPUT_FIELDS/Borders/Active | Mode | `c5aeea2b09a0207e2953e8d1befc2481c55eb72c` |
| INPUT_FIELDS/Borders/Disable | Mode | `c2c17970c9113cdaf7c53ddc5ff7918d4196b9fe` |
| INPUT_FIELDS/Borders/Error | Mode | `819a284b0c14f3113d614ee01368daf371dc06a1` |
| INPUT_FIELDS/Text/Place Holder | Mode | `e21567fc5e8a6695a9ca979319b408dfd58c5892` |
| INPUT_FIELDS/Text/Active | Mode | `1a965815e3b0860efe1927be7ab3b3b6863689ed` |
| INPUT_FIELDS/Text/Disable | Mode | `ce230480079285559d78f518a24eaa54307c7dfc` |
| INPUT_FIELDS/Text/Label | Mode | `6d7ff54162293ab9bad2e41a9cc9a4fbf48c077c` |
| INPUT_FIELDS/Text/Link field | Mode | `47cc0c93b5a1293ecc44947f9849f5357353c135` |
| INPUT_FIELDS/Text/Link field Hover | Mode | `39e7d9414356ecaf6171a562eabc187ebbf54e7a` |
| INPUT_FIELDS/Text/Link Field Active | Mode | `1bbb5a7563224496be63a3f39dbf41e385b9af47` |
| INPUT_FIELDS/Text/Link field disabled | Mode | `d320dee7ffdcf3fc676f0996f81e24fc8fb01af2` |
| INPUT_FIELDS/Text/Optional text | Mode | `74901cd5f417c01c3c8422c0f7c64bb2d5df9bc2` |
| INPUT_FIELDS/Text/Error Text | Mode | `58859395c7f40b1903cf299fe40a7c04aeaf7385` |
| INPUT_FIELDS/Icons/Place Holder | Mode | `d19e728d0ab5dc9a75f00b54d32cf78eafb72f23` |
| INPUT_FIELDS/Icons/Active | Mode | `885567f6f9b927091c927c6ca15c618e6f9d551f` |
| INPUT_FIELDS/Icons/Disable | Mode | `307e661335a610d1f49ffc9aa4110dddf5346905` |
| CHIPS/Background/Default | Mode | `66043fc5adedcbf6783001cb1dc02bc747fb6085` |
| INPUT_FIELDS/Icons/Label | Mode | `582e9d8e2d9dfa4c5a751ddb99770e07ad363542` |
| CHIPS/Background/Hover | Mode | `0ead6b920f4e4358ffce46f96b8d97eece77aa99` |
| CHIPS/Background/Disable | Mode | `56317bc6dfa91ce8561993955cf07d3c7304f6eb` |
| CHIPS/Borders/Default | Mode | `8d25e25ce197314b788105d71ba6188cd5f54f8d` |
| CHIPS/Borders/Hover | Mode | `2e772c15d81bc07496422432dd6c2ac050ce75e4` |
| CHIPS/Borders/Disable | Mode | `18ef846995bbbd95eaeb394b8a27a358f7fea15d` |
| CHIPS/Text/Default | Mode | `8440e0ab23fdd06dd682cf2456a5472cbe2d5e92` |
| CHIPS/Text/Hover | Mode | `76464ed724fd48b56940153c03285680d01973f4` |
| CHIPS/Text/Disable | Mode | `e5b1cfe520b4b086eb0d635603537e4be85d5736` |
| CHIPS/Icons/Active | Mode | `e1bd64b98e800d26a10d87aac1b2746df9bc3d97` |
| CHIPS/Icons/Hover | Mode | `2e08ccf1e7bbcc6178418e78a94db693ff6ddd98` |
| CHIPS/Icons/Disable | Mode | `df7392f260ac7b12791ecfb7bd3f51b8c9b4130f` |
| CHECK, RADIO, TOGGLE/Backgrounds/Default | Mode | `b50f3793697dbf74b694411e258f19853c47f8e9` |
| CHECK, RADIO, TOGGLE/Backgrounds/Hover | Mode | `735a4b18a9256392ffd7b55140556e29b841316a` |
| CHECK, RADIO, TOGGLE/Backgrounds/Disbale | Mode | `503bf43f792836ef637fa7584358052fba966899` |
| CHECK, RADIO, TOGGLE/Backgrounds/Click | Mode | `f345fd3bda8fcca1bf9f1caa2fc272f954681aee` |
| CHECK, RADIO, TOGGLE/Backgrounds/Click Hover | Mode | `c1598d2ccb46f242cbee8a01455eaaa9543ed956` |
| CHECK, RADIO, TOGGLE/Backgrounds/Click Disable | Mode | `6dd0ce21a5d86eb1f917615ad02eedada284c480` |
| CHECK, RADIO, TOGGLE/Inner For Check/White | Mode | `f782fce2c988e06035cf81c9f49c886ba1383f10` |
| CHECK, RADIO, TOGGLE/Inner For Toggle/Active | Mode | `66144ecdaf00dde4ac26f6f32df7f53120edf63d` |
| CHECK, RADIO, TOGGLE/Inner For Radio/White | Mode | `707e9ebfd565fcd7bb0fe9276433dcfbd1f4d271` |
| CHECK, RADIO, TOGGLE/Inner For Radio/Disable | Mode | `2ed99d3d5c6b606b9a652624bf1fa347e0ae94bf` |
| CHECK, RADIO, TOGGLE/Inner For Toggle/Active Disable | Mode | `16ce9443f70a862c9b6980be2d912cf94cb451c4` |
| CHECK, RADIO, TOGGLE/Inner For Toggle/Default | Mode | `f22bb5b116d41906a7197101f73ac56d574c29d1` |
| CHECK, RADIO, TOGGLE/Inner For Toggle/Hover | Mode | `4b6ad946463a76ce5f254ca9c8551e1ed5e6ef0b` |
| CHECK, RADIO, TOGGLE/Inner For Toggle/Disabled | Mode | `4434ed89907796337eeadd453b87c37ebe1225ff` |
| CHECK, RADIO, TOGGLE/Inner For Check/Disable | Mode | `33fbc5b73c3f11095bb6a61380b3d527615b7181` |
| CHECK, RADIO, TOGGLE/Borders/Default | Mode | `f30e4aa3a3bda83f62afbcc2725cd5d0a076f32b` |
| CHECK, RADIO, TOGGLE/Borders/Hover | Mode | `e82732a47acc657971b61a8f7a5417b5dae0dabc` |
| CHECK, RADIO, TOGGLE/Borders/Disabled | Mode | `9f8dbb4b1eed8a1232fdda3e0a17f753fa8df680` |
| CHECK, RADIO, TOGGLE/Borders/Outer Border radio | Mode | `46604bfb744d44110d2d05879845664c92db5f81` |
| MENU LIST/Background/Default | Mode | `fe46b30affd93a0ed29126a9cb1969e8b6f3feb4` |
| MENU LIST/Background/List Hover | Mode | `664a9eeb7fb8ebf2598d586e90d51bd0aea1f4f8` |
| MENU LIST/Background/List Selected | Mode | `0a4da841b9b5a16ec8d7c918b6abb72fdbb6c957` |
| MENU LIST/Background/Disable | Mode | `574364053a3d2e10a9256c8ba35744787a030158` |
| MENU LIST/Borders/Border | Mode | `9ab6624a6fe2d4254a0cab8f8c9088d69a4ecdf1` |
| MENU LIST/Text/Default | Mode | `d7ac65ea1b5a7feae0ee94572d247b36a9d00e6d` |
| MENU LIST/Text/Hover | Mode | `2e656314705b583e0a1149d42fc898a93936f3e3` |
| MENU LIST/Text/Disable | Mode | `5d9b846e23b2937d08a152f4317ce04d6f44f090` |
| MENU LIST/Text/Heading | Mode | `d1183de6a94558af5a65a773af2dbffaabb4ab5a` |
| MENU LIST/Text/Light text | Mode | `ed36b88552e5efcc8f8edcec3177051303f15c38` |
| MENU LIST/Icons/Active | Mode | `af23c7e395918134a61ef6a53e17398fbabd6d73` |
| MENU LIST/Icons/Hover | Mode | `2e444e407ff37736bfee0ea8f5d16d00e387b12f` |
| MENU LIST/Icons/Disable | Mode | `305a5690287b1c359835e50727c3579af9c4a7c1` |
| MENU LIST/Icons/Check deafult | Mode | `2e8cb6a1810c8955357d29645006fe06ebb6f569` |
| TABS/Primary/Background/Hover | Mode | `965755385dab38bebccbdfeba015007b3f948b14` |
| TABS/Primary/Borders/Default | Mode | `f4a1f532c0fa47a25d1a9b48e1e968f592712308` |
| TABS/Primary/Borders/Hover | Mode | `74965b8219482c5ee4678bd0456b265e82a70e01` |
| TABS/Primary/Borders/Active | Mode | `30a6038467779ed78409bc76f5a3b3029c03a0c7` |
| TABS/Primary/Borders/Disable | Mode | `8a2105ec3c9dbcc3cd6c555fd81e0b7e46d20831` |
| TABS/Primary/Text & Icon/Default | Mode | `f5fc0c507baf19fc18671d5d71d7cd99a54bb7b7` |
| TABS/Primary/Text & Icon/Hover | Mode | `d2e15c37a44b01d1776a515ae8b1ffb200f4efb2` |
| TABS/Primary/Text & Icon/Active | Mode | `ca6d55766091e15aa0eb9a539c5472bdcc0f3ddf` |
| TABS/Primary/Text & Icon/Disable | Mode | `b094ebbe0652c77a8857f25c0c3b46833ef6d9e5` |
| TABS/Primary/Background/Disable | Mode | `d79dd62c94cf62bcba1a7c689e5a0464e67cd581` |
| TABS/Secondary/Background/Active | Mode | `78b052b6a340849cc7f4fe9f1149bbc0b703184a` |
| TABS/Secondary/Background/Hover | Mode | `e42420a1f462964ec7e8b3c79b89c87ff0f0ed1d` |
| TABS/Secondary/Text & Icon/Default | Mode | `4fb70763520a3c191f0aaceb46c36f82195e874a` |
| TABS/Secondary/Text & Icon/Hover | Mode | `95e7577e6b2d67a024544e0b261d528c71232f76` |
| TABS/Secondary/Text & Icon/Active | Mode | `f3a15a84ceb046ecd1a844f8902f0385cc2f9f8c` |
| TABS/Secondary/Text & Icon/Disable | Mode | `25ab611fdc2601193ea46b808524d87c27cb3cce` |
| TABS/Secondary/Background/Disable | Mode | `3c5ce580839bf6905a94c35414ed6355ec1905da` |
| TABS/Secondary/Background/BG Default | Mode | `7fec9035d199e510c9e4ac5b476a3b9427b59a98` |
| BADGE/Background/Primary | Mode | `16089f5b5a3de16f9659f5a2708fb81d2bde45d4` |
| BADGE/Background/Green | Mode | `9ebef43d3e205f59a6583d26aacf0091708b623e` |
| BADGE/Background/Red | Mode | `1539e539c5987831c4f1f9977a3cb6df0bf88a57` |
| BADGE/Background/Pink | Mode | `b976cf4d60b82c364a132629287046741be4a70e` |
| BADGE/Background/Orange | Mode | `a7f8a9015ce096f451e963f0ace199b50edabdf2` |
| BADGE/Background/Grey | Mode | `7896b27087d7803310c1380d4592b1bdecd58c67` |
| BADGE/Background/Sec- Primary | Mode | `26d675e3e49dd9d0e1b533e6d79f6c87d7b8bae0` |
| BADGE/Background/Sec- Red | Mode | `ab8a554f61067ce0f11b590a9938485c4599f065` |
| BADGE/Background/Sec- Pink | Mode | `8b775220af01c61edd01723a2eba31953b29a5ed` |
| BADGE/Background/Sec- Green | Mode | `c3db28c422466b72853603cc358f99974342986b` |
| BADGE/Background/Sec- Orange | Mode | `53df569e80c12bfb593af76bf7f2cb15085e690d` |
| BADGE/Background/Disable | Mode | `9ee3e1165938224812a673a23a5972862a363926` |
| BADGE/Text/Primary 1 | Mode | `df68fc80638cf8327a079d88dd9e391d69584124` |
| BADGE/Text/Sec- Primary | Mode | `52b4c9d2f6980f0a107f68907fc6ee99359bc0fe` |
| BADGE/Text/Sec- Green | Mode | `4d7d6044e258ad0e0cc100160174d840f90d3a13` |
| BADGE/Text/Sec- Red | Mode | `67d68f4871449cc6a1dd88d949b6c21550363ada` |
| BADGE/Text/Sec- Pink | Mode | `8fc6c16bdfa6374a559a2a193633b6edbdf73aac` |
| BADGE/Text/Sec- Orange | Mode | `283e16ca793a59556548e343798b485b1bc0bee3` |
| BADGE/Text/Grey | Mode | `a17a93961c672bf70dc7e37c796d7d5b5b45690b` |
| BADGE/Text/Disable | Mode | `533300cf27df773248a81d1b3dcb7de916bb49a0` |
| BREADCRUMBS/Background/Hover | Mode | `d0087fc1c5beabcd4384eac970433f190ada0f6d` |
| BREADCRUMBS/Text & Icon/Default | Mode | `9158ef2606603de55c6f987c960a9a9695ab171c` |
| BREADCRUMBS/Text & Icon/Hover | Mode | `26662bd0d528f8679a412d703cf8f3ea5b0b4d75` |
| BREADCRUMBS/Text & Icon/Active | Mode | `42c876859c78b68d7176afa47d5eda4288d422e2` |
| BREADCRUMBS/Text & Icon/Disable | Mode | `2a8b7855f0c3a77bdcbc90e164891baefe4c357f` |
| ACCORDION/Background/Default | Mode | `e7a40947c5dbe3f94f5c2d639dd07b7f9c2ac71d` |
| ACCORDION/Background/Hover | Mode | `f91de10dff9a9ebd5e681e0f2939925fa845d50f` |
| ACCORDION/Background/Hover 2 | Mode | `8cece6799fecfe815c251ae8e0ab3ea69eaca3e4` |
| ACCORDION/Background/Active | Mode | `5ff3ad66cf6668b546825e61c7b22a3710f916cd` |
| ACCORDION/Background/Disable | Mode | `cb1eee83ace879864d0ee32524fbdafd57a5e26c` |
| ACCORDION/Background/Open Bg | Mode | `441bcee163ab82454d532ae2337cd3168e9faa92` |
| ACCORDION/Background/Icon Bg | Mode | `dcf5f53086021e727987adf72e93344dca51988f` |
| ACCORDION/Text & Icon/Default | Mode | `dd5fbe76e7f4db9c4891e5f624ef4cf4f1f8fbf2` |
| ACCORDION/Text & Icon/Secondary | Mode | `60c5b3b0439b72b5b93e06e5f3e1b468cd64bae4` |
| ACCORDION/Text & Icon/Disable | Mode | `a2706d3524d266dd0ef47fc56fb86577ed2c6317` |
| ACCORDION/Text & Icon/Secondary Dropdown | Mode | `3340e114743e6d83ff6e1ea06b339ac25b21b38b` |
| ACCORDION/Text & Icon/Secondary Dropdown Hover | Mode | `10d3479d222008b628a6e7505044ceaf44c1ee34` |
| ACCORDION/Border/Default | Mode | `c499a100e538ac8df7d26230e2fac45a05eb8294` |
| ACCORDION/Border/Disable | Mode | `3cac3c1d2eebd88e3dbbd3a79d988c2ce212b19e` |
| SIDE MENU/Background/Sidemenu Bg | Mode | `eee914c636e13f57a1c2998e5c12b841fb561d60` |
| SIDE MENU/Background/Menu Hover | Mode | `ce2bab60ba07a394ee0bc522433180d954e6f2b2` |
| SIDE MENU/Background/Menu Active | Mode | `143b5caf6af6731dba9ad53f0c6aeca1091f367a` |
| SIDE MENU/Text & Icon/Default | Mode | `0c9c338f9336d79ef1de1bf7e024972e9132d882` |
| SIDE MENU/Text & Icon/Hover | Mode | `26e694943442556642a811290e36314a1c8b9b49` |
| SIDE MENU/Text & Icon/Active | Mode | `a603977717f6a54dec69e7acb87122b129bd9435` |
| SIDE MENU/Text & Icon/Disable | Mode | `fc1b2400830acde4c8406ce7156d3dcad76c7bf1` |
| SIDE MENU/Text & Icon/Sub Heading | Mode | `f5af51bde7bdb3b77d518a917017b6c36f0bc34e` |
| SIDE MENU/Text & Icon/Service Name | Mode | `5fbe48b7ee437f91327a3bb5dd13c05887ccf54d` |
| SIDE MENU/Borders/Default | Mode | `f2a52ab89f98e1df3a9caaceea12e9dd00c16441` |
| BRANDING ICON/Icon Color/Blue | Mode | `470ccc11af67b94d38375c655263d2d2dd923b2d` |
| BRANDING ICON/Icon Color/Red | Mode | `8fa6ccab91def9f2e89117ed6cd2e9292433460b` |
| MAIN HEADER/Bg/Bg | Mode | `547d945988fbd0ee6a6cced0cb1f5e0d10995659` |
| MAIN HEADER/Project Name Logo/Bg | Mode | `79286b939d75f0690366621b01dc450f65831e57` |
| MAIN HEADER/Project Name Logo/Text | Mode | `292e51342d60e42299f92dcf149572d2ed84f3d3` |
| MAIN HEADER/Border/Border 1 | Mode | `ad241d93ce1a2d0b4273189ffa5e964698b3a1e5` |
| SUB HEADERS/Bg/Bg | Mode | `d01fc49e637422c2a4171176d4fce1a12a224d26` |
| SUB HEADERS/Border/Border 1 | Mode | `189f79e777bc253d047d1e8f9dad668ab2437299` |
| SUB HEADERS/Text/Border 1 | Mode | `4cc977306cf95da36ba1493bd29702fb7083bcf4` |
| FULL PAGE POPUP HEADER/Bg/Bg | Mode | `bef107aa39602542d50eabd56ff28fed126dbee9` |
| FULL PAGE POPUP HEADER/Bg/Bg 2 | Mode | `bcfd72e1a8d9593dd5895a96a52d3f17c389d5b3` |
| FULL PAGE POPUP HEADER/Border/Border 1 | Mode | `f5c07b6f02894efdb21c46f0c294a481b30c7501` |
| FULL PAGE POPUP HEADER/Text/Text | Mode | `29e235fe4e899b3193ce2a4db3c4a72ff9d2ff6e` |
| SERVICE_MENU/Borders/Side Border | Mode | `b8513a0147732c16d79ee53efadf32acf966c9c4` |
| SERVICE_MENU/Icons/Service icon Default | Mode | `6e2dbd99ba5fa467e7f9e686fa77155924ce5318` |
| SERVICE_MENU/Text/Sub Heading | Mode | `1a241e39e36a0c11ac1d872a3c990d9958157a61` |
| SERVICE_MENU/Text/Default | Mode | `c029d706a61281889336dea8cbcf091694af7b88` |
| SERVICE_MENU/Text/Active | Mode | `174bb7a2043854f679b0afa6afcec7f364010fc9` |
| MAIN HEADER/Text/Project text | Mode | `32cb2565a9948c5456958bac488f1a27f597df92` |
| BUTTONS/Outline/Bg/PrimaryHover | Mode | `24c01c3bf8ac3d65d406f03b5a6e4a62ef1599e6` |
| BUTTONS/Outline/Bg/SuccessHover | Mode | `9fa3619c27be827a1d88209dd36bcd992b5bf1ad` |
| BUTTONS/Outline/Bg/DangerHover | Mode | `51138d0fa0764e851253328b719911ed18ecbd9d` |
| POPUP/Border/Border | Mode | `c8300c44a50fce5e4e3ad397ea0953fee3ef9802` |
| POPUP/Border/OuterBorder | Mode | `b489c5076d8419cf2723c453fd39369aa854ddf7` |
| POPUP/Bg/Bg | Mode | `25df50a797f0c5a6258ea61edc58a421d41b493c` |
| POPUP/Blur Layer/Bg | Mode | `993165bacaa00efaea61a575ac13ab78c5e6335a` |
| ATTENTION/Info/Background | Mode | `d62baa85304c9a907c55a5ba4349d2b70822131c` |
| TOAST/Default/Background | Mode | `7556cc809c5f66b4961d92436ac9661e18872c38` |
| TOAST/Default/Border | Mode | `f40ad4bda3e566bca26d9d56ec33e28ffc7708ca` |
| TOAST/Default/Icon, Line Success | Mode | `1169fac02adc3932c5ca58c503f78a59a627227f` |
| TOAST/Default/Icon, Line Danger | Mode | `4a4203f61a7c28a709ad3bbcd6bae298b2affa75` |
| TOAST/Default/Icon, Line Info | Mode | `5b95ca5839f22ea8e8597cf99242bd14e46a457e` |
| TOAST/Default/Icon, Line Warning | Mode | `87144bd21f1d6634bf1e388d2422ca5c0eaf2585` |
| TOAST/Default/Text Primary | Mode | `54b626c9b5bd5e13312000aab24c443e8aa2be99` |
| TOAST/Default/Text Secondary | Mode | `c5dbd56e8b33d130ee1df6723e53593892e10d75` |
| ATTENTION/Info/Border | Mode | `e2351aef06d3156eb28226025097348e71d0ed5e` |
| ATTENTION/Info/Text Primary | Mode | `dc4a3525cc1fd22ff48bf4dbff26e44e7a1c023b` |
| ATTENTION/Info/Text Secondary | Mode | `f8704ce9737819c013ee323b4a304ed0b4e10957` |
| ATTENTION/Info/Icon | Mode | `0de5021d72e734a401d26497dcf423e6408551f3` |
| ATTENTION/Danger/Background | Mode | `424e1b41141a67edbb7d02159176dd8b6fd975be` |
| ATTENTION/Danger/Border | Mode | `71c0377f3444d6dd4ecb563a95ab9bb783023be3` |
| ATTENTION/Danger/Text Primary | Mode | `a42bde4fc26055d36386a77c620c0ddf90a33625` |
| ATTENTION/Danger/Text Secondary | Mode | `2ba40dc770b39140c8034af2b0f066146c103b52` |
| ATTENTION/Danger/Icon | Mode | `160a3b21ddf50d5c39c3820bfc941983902686ab` |
| ATTENTION/Success/Background | Mode | `b4d29fdf80ad61b7db0ed2856351575beef4bb11` |
| ATTENTION/Success/Border | Mode | `6757574ac37bd465ee29449c8606d518b668e2b1` |
| ATTENTION/Success/Text Primary | Mode | `0d29ecb2f606d72d298e5921695dd6d6e4b6c816` |
| ATTENTION/Success/Text Secondary | Mode | `705df56cd9e6e12f6c0c3f6d331f09b550ce292f` |
| ATTENTION/Success/Icon | Mode | `6de3412e55948904e121f1b9b7c2e53cd20fac4c` |
| ATTENTION/Warning/Background | Mode | `dd1e11ec5d49784b5f77a9590bfd532fe7dd09d6` |
| ATTENTION/Warning/Border | Mode | `a8281aaf031c3ac9ca1281eac223ee6c73489d0d` |
| ATTENTION/Warning/Text Primary | Mode | `d9dcd7c1625cb8da90115c49fb4dc285f20c67dc` |
| ATTENTION/Warning/Text Secondary | Mode | `13472faee69843f5d0df94e34638d3c2d9777072` |
| ATTENTION/Warning/Icon | Mode | `6a256d7e5a427b2d0026c8bb5a7d4d04bfc1d6a4` |
| PAGINATION/Bg/Background | Mode | `8f22741a5c3fb9b5a499750726ec88a9ec172317` |
| PAGINATION/Bg/Text Primary | Mode | `3d687051bfa5cde604fc3e5ec013883c9e2e7539` |
| PAGINATION/Bg/Text Secondary | Mode | `9c27e51dc44ccf667622c7c00163df3e2ade2877` |
| PAGINATION/Bg/Text Teritory | Mode | `e22a0b52a671f30d0518394095f69134d167eb26` |
| PAGINATION/Bg/Theme | Mode | `c2bf50dd3c9b7a495bab94d7087678f7ab1f9bc7` |
| PAGINATION/Bg/Divider | Mode | `445381ab8550bda0a9d8817c60d5748ead26e93e` |
| TOOLTIP/Static/Background | Mode | `825c222acb6afcdfac777ec638509fa570a13b70` |
| TOOLTIP/Static/Text Primary | Mode | `81a642904fcc62eb490a9f85ab391bb2c9c3751d` |
| TOOLTIP/Static/Border | Mode | `50bdb8009e65ef1ae7768e9b26ff507041e8d9d1` |
| TOOLTIP/Static/Text Secondary | Mode | `cebe62e055c6a748af1027b9d68a730105d964d5` |
| LOADER/Content Loader/Primary | Mode | `7a3a0cef901d8917351c8b85e191a3d3383dd9d1` |
| LOADER/Content Loader/Secondary | Mode | `014f7d2521c83a177100c5b6de0303291002c696` |
| LOADER/Round Loader/Primary | Mode | `a16236e20b8a02626f97b09dead4921e147e7f5e` |
| LOADER/Round Loader/Secondary | Mode | `d4dd59c908e587749888772036879eb2e46fc681` |
| LOADER/Round Loader/Teritory | Mode | `580efb0db33b0756a40bd952ea640d3bf53a8aa8` |
| LOADER/Progress Loader/Primary | Mode | `c96cf9dc66f8b98ec2c4486202b8eda883eb63b2` |
| LOADER/Progress Loader/Primary 2 | Mode | `cc11ccf9893bc0178f76cc6e5479ea01ab7477d9` |
| STEPPER/Bg colors/Default | Mode | `5bcda7175a9dd7b32a43605ec596af170d638bcc` |
| STEPPER/Bg colors/Active | Mode | `b3926f9d4984b459411e7a6556a15f104210e5e5` |
| STEPPER/Bg colors/Completed | Mode | `3683a86ee4781ddabf5f8a92425b920ab7b1037a` |
| STEPPER/Bg colors/Disable | Mode | `30a4113b98e8bd247b01e591bb5118cf6c5f6917` |
| STEPPER/Text/Default | Mode | `78a33196e05188d51ef92992fbb0b48fcaac0871` |
| STEPPER/Text/Sub Text | Mode | `5fde63884a397f70b44df3c3bd759f01ab9dd362` |
| STEPPER/Text/Active | Mode | `a80bf1f7f4ddb35364318d12d47d4641ac44fcee` |
| STEPPER/Text/Completed | Mode | `150c79ac6d7f5c3567690e2358da408f1d23613e` |
| STEPPER/Text/Disable | Mode | `a048c6a611808b2ccc9f4a97c014ba4b356c1436` |
| STEPPER/Text/Numbers | Mode | `ba20773e04ae1fb95d00fae06c51e6a8e36d9858` |
| STEPPER/Divider/Default | Mode | `f01deeabc27d44020a616566ff01e209deabd16f` |
| STEPPER/Divider/Active | Mode | `026886d4cb92b08d2419b82e93712ccc61dc2a75` |
| STEPPER/Divider/Completed | Mode | `6c39c4da90c929a7a4b4f25583994322126aaf01` |
| STEPPER/Divider/Disable | Mode | `8e217d8f9402bb624a82f00a41cea754e56d2368` |
| STEPPER/Borders/Default | Mode | `4e7475919a40fc09a8803901559adb48aebdda13` |
| STEPPER/Borders/Active | Mode | `67393a8a35cd23ebc76a6a9612fb8f1f2d9a77ad` |
| STEPPER/Borders/Disable | Mode | `ebe6232bc15c9f776ab5bfa51ed8d72c55e29721` |
| AVATAR/Bg colors/Default | Mode | `601bd9c4b76f7925822f3055063cd1fa72d21714` |
| AVATAR/Bg colors/Default 2 | Mode | `dbfb3659f7302ffcc8322c10111c764fe76d1ab6` |
| AVATAR/Icon/Avatar | Mode | `1e94f40c0e848ef518e8dda37946e36475c64551` |
| AVATAR/Borders/Default | Mode | `a543012433a325e7bbfca97085cf1102d7085592` |
| AVATAR/Borders/White | Mode | `7f4cb4123419a90b863af28e7c8893c02d0a951d` |
| BADGE/Border - Removed in UI/White | Mode | `d118d64a34002da4f101cf5a6dc452076aa22b1b` |
| BADGE/Border - Removed in UI/Disabled | Mode | `89b2609be7662c732b7794e8e86d7b689cdc6d33` |
| CODE BLOCK/Bg colors/Writer | Mode | `c728f4e5b32b4e0b613841179bae024f1deaf5bf` |
| CODE BLOCK/Bg colors/Reader | Mode | `2307f7211812522dccf2f229ca1c29be86fbd03c` |
| CODE BLOCK/Borders/Default | Mode | `6f99fdb0966702c13da1ae9fc15b32d59c7bda49` |
| BUTTONS/Gradient/Text & Icon/Default | Mode | `a8868894643160dec8e18d89bf171fb28b387189` |
| BUTTONS/Gradient/Text & Icon/Hover | Mode | `9ba9b7fe49c21770845691aedd2a2759ce3f9906` |
| BUTTONS/Gradient/Text & Icon/Click | Mode | `b3048b7f56401e0157f9efebace6a85bda981fdb` |
| BUTTONS/Gradient/Text & Icon/Disable | Mode | `0eb818b05e70de5bbbe98305714ca16819a3c9a1` |
| BUTTONS/Gradient/Bg/Gradient top | Mode | `b0404896c72b932be971feed03e2a4c2b18552fb` |
| BUTTONS/Gradient/Bg/Gradient bottom | Mode | `a3fac0c1a8235e4d11705cc2d240037e3bfefecf` |
| BUTTONS/Gradient/Bg/Gradient top hover | Mode | `d21ab45a3109be782da59a578c007d4358e82ce5` |
| BUTTONS/Gradient/Bg/Gradient bottom hover | Mode | `3133834772b6255f1408c96b155af1930b37c004` |
| BUTTONS/Gradient/Bg/Gradient top Click | Mode | `4407556520ffdb22afe941dfb474148ebc43df3f` |
| BUTTONS/Gradient/Bg/Gradient bottom Click | Mode | `3bdb4ad76db300e7490cbc9e63bf3ab93d75635a` |
| BUTTONS/Gradient/Bg/Gradient top Disable | Mode | `54b59c9aeb6f3aa3f0adb6af168416b12293b495` |
| BUTTONS/Gradient/Bg/Gradient bottom Disable | Mode | `fa430711322ed3cb2303052967592d752e97b88c` |
| LINK BOX/Background/Default | Mode | `fd3c75cd32e7b6ed8e7aed79ff8bfe700685f1f4` |
| LINK BOX/Background/Hover | Mode | `154fed6aba00a7df9a73529c639d5daad775e1c4` |
| LINK BOX/Borders/Default | Mode | `1abe07c80a3a3858606b3d08abcad8aff1a4963c` |
| LINK BOX/Borders/Divider | Mode | `d57247d806a82401bcc2ec2d5f4d63fe3ca886e7` |
| LINK BOX/Borders/Hover | Mode | `89594295463f3c307124d8bb9d3aa0d7b0c6bffa` |
| LINK BOX/Text/Label 1 | Mode | `84515f65759a747435b2ed3c94cf4c5e1a0691a7` |
| LINK BOX/Text/Label 2 | Mode | `c66004599043378f5da3995564f5b5ae4c892f67` |
| LINK BOX/Text/Main Text | Mode | `b45c9d749256c023d8a2b72b7a862d566788ed19` |
| LINK BOX/Icons/Label | Mode | `9c21cad84263f6985f82ac2451fd00a5545df239` |
| LINK BOX/Icons/Default | Mode | `c5b14746123229ffb7edd6f3002540efe42998d6` |
| LINK BOX/Icons/Hover | Mode | `c2fbe14f0d8fe8613fd2b0b26752c5e134d5a010` |
| LINK BOX/Icons/Click | Mode | `2807479ad260159edeb209f62978b7a93282ebf4` |
| DATE PICKER/Background/Datepicker Bg | Mode | `be52fe1a691afc57720e11c29352bf566fb008cc` |
| DATE PICKER/Background/Number Hover | Mode | `cf965cc3ed5cd147356c0e185bc45b6499ec3495` |
| DATE PICKER/Background/Number Selected | Mode | `ee9b8fb2b55dd13598651992a53c70af1a1f2280` |
| DATE PICKER/Background/Number Active | Mode | `750d81fd1ef453051957b82c5ad88fda9a674742` |
| DATE PICKER/Borders/Outer | Mode | `9bec599768a7c6c450e21f285998d9ecf5f09c04` |
| DATE PICKER/Borders/Line | Mode | `04f1a3a99fce4f5820d2d6196aa91ace69e6680d` |
| DATE PICKER/Text/Default | Mode | `2f4bfc9d1769fc2245da87baec7a6b24d697c171` |
| DATE PICKER/Text/Selected | Mode | `3214d0a66d829c64d8c57c0ce33062164966da17` |
| DATE PICKER/Text/Active | Mode | `d461dbd4816f6cbeccb9e7ccb9d52d267bbf3e96` |
| DATE PICKER/Text/Disabled | Mode | `9ddea429f6b57a1bbcedb467e8bccf23a47b455f` |
| DATE PICKER/Text/Days | Mode | `7cdf0ca0675e4ee268154d61c31a225068a6360e` |
| DATE PICKER/Text/Headings | Mode | `8527bddb85863614d08a3d013bbc10c182a6daa0` |
| OTHER SHADES/Green/Green 1 | Mode | `c5b468027686a2c9dc6e05aeac52f132148b8770` |
| OTHER SHADES/Theme/Theme 1 | Mode | `ce98fc91700925c5828b0649694ce8d694537610` |
| OTHER SHADES/Theme/Theme 2 | Mode | `724edb6d513653fe7c756c00ced1f1c64442a62f` |
| OTHER SHADES/Theme/Theme 3 | Mode | `0efe8122b8b247c501d7c3b86d7b86778da39c5b` |
| OTHER SHADES/Theme/Theme 4 | Mode | `73e778f18003828628514fd853d9c370db0f4ae3` |
| OTHER SHADES/Green/Green 2 | Mode | `40849375c32981085e8e783ba6623159e5ea1053` |
| OTHER SHADES/Green/Green 3 | Mode | `9cafffd784620e8167db4cada823dc2ece7e0dba` |
| OTHER SHADES/Green/Green 4 | Mode | `f83e5196695146c60ada6141fc9037940c520346` |
| OTHER SHADES/Blue/Blue 1 | Mode | `95d832925658f8f91a44bb6412c1d3eb2ac85191` |
| OTHER SHADES/Blue/Blue 2 | Mode | `c1004017436b3871c45dd1cf8525b9cff28a50a6` |
| OTHER SHADES/Blue/Blue 3 | Mode | `bda60cd8938dfeeaa41b13a9ea7d70e70d16721b` |
| OTHER SHADES/Blue/Blue 4 | Mode | `2b11eff9da2daccccafb0366cfa08147a754707f` |
| OTHER SHADES/Pink/Pink 1 | Mode | `885bdc052f6b6a913b694836d2c63fff40932309` |
| OTHER SHADES/Pink/Pink 2 | Mode | `8f24525c312d3d78007b1cc43ea0243545884080` |
| OTHER SHADES/Pink/Pink 3 | Mode | `b62095d1546e02fa5f3b82b2e9208996fb845ee3` |
| OTHER SHADES/Pink/Pink 4 | Mode | `3498a4485c80b7156b74a80af5f9d0e792759554` |
| OTHER SHADES/Orange/Orange 1 | Mode | `d1a680043888628f6988e070a825a235984cc094` |
| OTHER SHADES/Orange/Orange 2 | Mode | `828eb10cc3e1a5c19391df586e6147763dd8b90b` |
| OTHER SHADES/Orange/Orange 3 | Mode | `a8c2574fd9a05b1d89376af170330b8b4345ca72` |
| OTHER SHADES/Orange/Orange 4 | Mode | `196dd6808474b55bb51f7959f6884c003909651c` |
| ATTENTION/Default/Background | Mode | `50bc0bb5cc09351626001cb38ec893df7ddca87a` |
| ATTENTION/Default/Border | Mode | `7b4ab38e96047a2a8a085825ad5a1407d2c83bab` |
| ATTENTION/Default/Text Primary | Mode | `3b0eac94091ca0a58dfcd6bacd390310801206ca` |
| ATTENTION/Default/Text Secondary | Mode | `a6697465729a5dda84fac0df55073145d8633c94` |
| ATTENTION/Default/Icon | Mode | `9ceb3067d39dbefafc7f2e7d416e83c2c657f06b` |
| CAROUSAL/Carosual default | Mode | `bbe5c3c7ccbd0eadbf5435d1a095323a1ecd6046` |
| CAROUSAL/Carosual hover | Mode | `93b4135fe0f6f136dcefe5c86e312e4df05d6ae9` |
| CAROUSAL/Carosual Active | Mode | `21b274f1af2f296649ab2844a10c699269656db1` |
| TOUR/Background/default | Mode | `e8b7b291141d0b26dd0164b3d3bf36104276914a` |
| TOUR/Background/Blink bg | Mode | `0f91ea3de06f0a71e2f2823b3269ae344ba13dfa` |
| TOUR/Borders/Outer | Mode | `a5edfb9be6626a5fee1951e6144a3e7e0ae985b8` |
| TOUR/Borders/Blink Border | Mode | `60cde610bc97405d7b0c534a72f0f19547bd6305` |
| TOUR/Text/Heading | Mode | `f099aa0ba979952f876a90d25bda69620f164934` |
| TOUR/Text/Sub Text | Mode | `67c64a0f62add9669841261c9af86e10c0f6db8c` |
| TABS/Secondary/Border/Default | Mode | `aa5903f068374bfcb76fd6ee5ecc98cc98cd5fa3` |
| PROFILE NAV/Background/Profile Area | Mode | `fcae28ef23feb02c6820496f1dfb8c733df98e92` |
| PROFILE NAV/Background/Appearance Light | Mode | `e377bd90943941c48536923b04e7841870ca0d80` |
| PROFILE NAV/Background/Bg Appearance Light | Mode | `800ef8dc95a9574f4bb8ab88cf24e8d9c54880a4` |
| PROFILE NAV/Background/Line Light 1 | Mode | `099b41538332666f78081716acfbe605c38248d6` |
| PROFILE NAV/Background/Bg Appearance Light 2 | Mode | `eaed157a68e5790088c502433013358d54517a39` |
| PROFILE NAV/Background/Line Dark 1 | Mode | `a2b463796c04c7d7ade31197d11777e54451232b` |
| PROFILE NAV/Background/Bg Appearance Dark 1 | Mode | `1357acb5153a99ce083d7cfcf3df2757cd24a076` |
| PROFILE NAV/Background/Appearance Dark | Mode | `01a52ea238c6c7cf3e665b7631074e8819cf9ac3` |
| PROFILE NAV/Background/Bg Appearance Dark | Mode | `b2dadeb1c2fb2793aae21575c79e43bf3eacdcd2` |
| PROFILE NAV/Background/Theme | Mode | `786638a078e171cb8357c94dd1cc236067dd4a07` |
| PROFILE NAV/Background/Theme 2 | Mode | `7ff47c93bcc0ed1dca2ad1619d16a49532508f93` |
| PROFILE NAV/Background/Whilte | Mode | `9e5e229638e72ddcb42780a826f96d6f34eee2f9` |
| PROFILE NAV/Borders/Border | Mode | `6a21278d173cb89688d08d9360bc555acb8054d7` |
| PROFILE NAV/Borders/Outer border | Mode | `a1675c47accef7b2fc4885c5c4d6fcab84f9dd12` |
| PROFILE NAV/Text/Heading | Mode | `9cc4b2079e2911477633abab34a5281d5d85e8d7` |
| PROFILE NAV/Text/Sub Text | Mode | `92ab28854c2b60ff26afa046212e33f7db808c61` |
| PROFILE NAV/Icons/Light | Mode | `729542a5383a0090158867c4aa57b7a333f04d5a` |
| PROFILE NAV/Icons/Whilte | Mode | `24a55028a306a5a56c60800192151ecdc2d96b5c` |
| PROFILE NAV/Icons/Primary | Mode | `98dfb37184201b27bb970b2e5ade2d3140dd885b` |
| TIMELINE/Background/Green | Mode | `056da3a853ef702c3cc7502fde2a623285422f2a` |
| TIMELINE/Background/Green Dot | Mode | `162e9615f8b20655362cc75e4ded5473afe1ffb2` |
| TIMELINE/Background/Orange | Mode | `d2e4a3fc41d2267936689a81e2b5896f7184b2c0` |
| TIMELINE/Background/Orange dot | Mode | `176c3d86f51c5ba66497490efdf8efe395f55622` |
| TIMELINE/Background/Blue | Mode | `2c41a0f65cdfdd718ce549ea685085f477fce8d9` |
| TIMELINE/Background/Blue Dot | Mode | `c8cc67edc1c7f5bcfdd645ff259a733db673fbe4` |
| TIMELINE/Background/Red | Mode | `49c52d0f44625eaf81ffb22f01cbe8e3ca09e463` |
| TIMELINE/Background/Red Dot | Mode | `ddde92de0050583afb06fe8436e2d438831e4e9c` |
| TIMELINE/Background/Grey | Mode | `1360bee496b2c1af9bdc4c2ae83fdd5729ea608a` |
| TIMELINE/Background/Grey Dot | Mode | `312d4c73cbed610b1b72c6d2a14d7d434a287564` |
| TIMELINE/Line/Default | Mode | `315da92de67594c72e3baecf3513932a3588e4ae` |
| TABS/Code Tab/Background/Active | Mode | `250e8bd2d6979b865f5a184b97332f163a509c3c` |
| TABS/Code Tab/Background/Hover | Mode | `bbf8fd0eaf020eb7ed172fd7f08c6a08fa9d8d96` |
| TABS/Code Tab/Text & Icon/Default | Mode | `c95916476958fb7dcdd19f7f1079f6104b86dfed` |
| TABS/Code Tab/Text & Icon/Hover | Mode | `9ba58d09782325c2d058814fe19ef69219effdac` |
| TABS/Code Tab/Text & Icon/Active | Mode | `76bddc950f856bdbb632956fe003a707d9f26570` |
| TABS/Code Tab/Text & Icon/Disable | Mode | `7a098792c1d96086e14ab6957ff89995e19f62f7` |
| TABS/Code Tab/Background/Disable | Mode | `d8dc0b0076a3c437fd2fecb23c28763171e052f8` |
| TABS/Code Tab/Background/BG Default | Mode | `fcb7968552cd7c44308ef49abe3636e721643edc` |
| TABS/Code Tab/Border/Default | Mode | `75b5e93945da20ce3a89c3e2a19a0479ba0ff055` |
| OTHER SHADES/Purple/Purple 1 | Mode | `09b0d27004fca34fdd00443ead114b1ee8b43a3e` |
| OTHER SHADES/Purple/Purple 2 | Mode | `d4b9920aceae4c889e0efd145d35b0fcc3bc4f7a` |
| OTHER SHADES/Purple/Purple 3 | Mode | `da31cc0cd2ae118cdb6fb8e8e2e0c1b2af6fb784` |
| OTHER SHADES/Purple/Purple 4 | Mode | `d35755f99574efc476cc4401744ef612fcae2291` |
| GRAPH/Text/Text 1 | Mode | `ba4feaa74a43e390cc6e17c86a17f88ed977dcb1` |
| GRAPH/Text/Text 2 | Mode | `80c1424f11923a79e4b84a6b3a644bcf9d029e9c` |
| GRAPH/Text/Text 3 | Mode | `a342398d7633e44b11d58b40d2100c852affac47` |
| GRAPH/Lines/X&Y Axis | Mode | `b9c1eded6a483e2a286ac25e3f6bd6535f46c2cd` |
| GRAPH/Lines/Line 2 | Mode | `cd6ccd0bcd302ed179d08548305be510242e11f6` |
| Default - RoyalBlue/L Primary | Theme | `0017910cc3ec08a51b4c8944a36eb2db52c887e3` |
| Default - RoyalBlue/L Primary 2 | Theme | `702c6244c327d3b9b751a2854b38702f366eca73` |
| Default - RoyalBlue/LPrimary 3 | Theme | `50796799a53224c25523c5fcd783b985b2fb1e24` |
| Default - RoyalBlue/L Primary 4 | Theme | `d4a1d439b9fae7252d2ffcd17916d8ca92c1282b` |
| Default - RoyalBlue/L Primary 20% | Theme | `7b68557c4811492f710f6f588f6fea5e58c513c5` |
| Default - RoyalBlue/D Primary | Theme | `111e066b869bc270e4181494e609944b29e73aa9` |
| Default - RoyalBlue/D Primary 2 | Theme | `62e1772fb2f409578277b101a379a9e1a7273cb7` |
| Default - RoyalBlue/D Primary 3 | Theme | `44bc818f88de0bec491ea8e95b94a9558472cca7` |
| Default - RoyalBlue/D Primary 4 | Theme | `98ea108edb80dbced9210f8bde974728635f58f0` |
| Default - RoyalBlue/D Primary 20% | Theme | `855a0973d201781896b9fcf1ed80ab45e4d31e3b` |

</details>
