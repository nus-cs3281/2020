### Project: TMK/QMK

TMK is a keyboard firmware with useful features for micro-controllers started by [@hasu](https://github.com/tmk), a keyboard enthusiast in Tokyo, Japan.
QMK branched out from TMK to offer support for proprietary keyboards from certain Western companies. 

TMK/QMK goes beyond providing basic functionalities but also allow users to customize keymaps.
Keymaps allow for fine control over the keyboard where anything from LED light patterns to OLED screen displays can be customized.

### My Contributions

I prepared a patch to enable two-way communication between a [Lily58 keyboard](https://github.com/kata0510/Lily58) and the computer, displaying output on the two LED screens attached. 
This is achieved by having a HID server running upon OS startup to ping the keyboard with an initialization packet to start the exchange of data. 

Unfortunately this relies on the new split-keyboard API, a [PR](https://github.com/qmk/qmk_firmware/pull/6260#issuecomment-620291169) which was proposed in July 2019 and just got merged on May 2020.

### My Observations

TMK is sparse in documentation and contribution guides.
Potential contributors are recommended to reach out to @hasu before even opening a PR.
Otherwise, [PRs](https://github.com/tmk/tmk_keyboard/pulls) are simply ignored due to lack of attention and manpower. 

As a result, the barrier to even start contributing to TMK is extremely high.

On the other hand, QMK made the decision to allow all contributors to commit their own flavor of keyboard firmwares into the main repository.
Not only that, each keyboard firmware contains [multiple user submitted keymaps](https://github.com/qmk/qmk_firmware/tree/master/keyboards/lets_split/keymaps) which rely on the API to provided personalized features.
Over time, hundreds of firmwares and keymaps have accumulated and every future change must either not break existing code or be changed with permission from the initial contributor.
End users will end up pulling unnecessary files too.

This extra burden offers little convenience to end-users at the overhead of slowing down project velocity by orders of magnitude. 
I would suggest abstracting the drivers of QMK out into its own repository and having manufactures/users import that as a git submodule.