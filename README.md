<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Allinmi kanman nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) ñawpaqta churay, chaymanta `direnv allow` qillqana mayt'uman yaykuspa ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) kikinmanta ruwasqa kanqa willañiqiman yaykuspa).

Niyta munan: Chino simiman tikray japonés, coreano, inglés, inglés simiman tikray tukuy wak simikunaman. Chino, inglés simillata yanapayta munanki chayqa, `zh: en` nisqallata qillqayta atinki.

Niyta munan: Chino simiman tikray japonés, coreano, inglés, inglés simiman tikray tukuy wak simikunaman. Chino, inglés simillata yanapayta munanki chayqa, `zh: en` nisqallata qillqayta atinki.

* [ñawpaqninpi kaq codigo](https://github.com/xxai-art/web)
* [Simi paquetes llapan sitiopaq](https://github.com/xxai-art/web/tree/main/i18n)
* [Yaykuna módulos kaqpaq simi paquetes](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Web nisqapi Achka simipi Qillqakuna](https://github.com/xxai-doc)

Ñawpaq kaq programacion simiqa [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , wakin ruwanakunata yapan coffeescript sintaxis kaqpi, qhaway [./coffee_plus.md](./coffee_plus.md) .

## Web kitikuna, qillqakuna ima internacionalización nisqa

Kay 3 proyectokunapi hatarichiy

* [@w5/mdt nisqa](https://www.npmjs.com/package/@w5/mdt)

  Sufijoqa `.mdt` , `<+ ./coffee_plus/import.js>` nisqaman rikch'akuq sintaxis nisqawanmi hawa willañiqikunaman riqsichiyta atinki, chaymanta `.md` k'askaqwan markdown nisqatam paqarichiyta atinki.

* [@w5/trmd nisqa](https://www.npmjs.com/package/@w5/trmd)

  Markdown tikrayqa manam codigokunata chaymanta t'inkikunata tikranqachu, chaymanta tikrasqa rimaykunata waqaychanqa. Sichus t’ikray hukchasqa kanman ichaqa ñawpaq qelqa mana hukchasqachu chayqa, hukmanta ruwaspaqa manan t’ikrakuypa t’ikrakuynintaqa qelqanqachu.

* [@w5/i18n nisqa](https://www.npmjs.com/package/@w5/i18n)

  `yaml` ruwasqa web kitikunata tikranapaq simi willañiqikuna.

### Qillqa tikray Automatización kamachiykuna

Qaway codigo waqaychasqa [xxai-art/doc](https://github.com/xxai-art/doc)

Allinmi kanman nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) ñawpaqta churay, chaymanta `direnv allow` qillqana mayt'uman yaykuspa ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) kikinmanta ruwasqa kanqa willañiqiman yaykuspa).

Pachaknintin simikunaman tikrasqa hatun codigo base nisqa mana kananpaq, sapa simipaq sapaq codigo base nisqatam ruwarqani, chaymanta codigo base nisqa waqaychanapaq organizacionta ruwarqani

Pachamama tikraq `GITHUB_ACCESS_TOKEN` churay chaymanta [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) purichiyqa kikillanmanta codigo waqaychasqa ruwanqa.

Chiqamanta, huk código base kaqpipas churayta atikunki.

Tikray qillqap riqsichiynin [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Qillqap chiqanchayninqa kayhinatam t'ikrakun:

[bunx](https://bun.sh/docs/cli/bunx) nisqaqa npx nisqap rantinpim, aswan utqaylla. Chiqamanta, sichus mana bun churasqachu kanki, chaypa rantinpi `npx` llamk'achiy atikunki.

`bunx mdt zh` `.mdt` nisqatam zh sutiyuq willañiqipi `.md` hina ruran, uraypi 2 t'inkisqa willañiqikunata qhaway

* [kaphiy_aswan.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [kaphiy_aswan.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` tikraypaq ukhu codigo (sichus `nodejs` churasqa kanki, ichaqa `bun` chaymanta `direnv` mana churasqachu, `npx i18n` purichiyta atikunki tikraypaq).

[I18n.yml nisqatam](https://github.com/xxai-art/doc/blob/main/i18n.yml) t'aqwinqa, kay qillqasqapi `i18n.yml` nisqap wakichiyninqa kayhinam:

```
en:
zh: ja ko en
```

Niyta munan: Chino simiman tikray japonés, coreano, inglés, inglés simiman tikray tukuy wak simikunaman. Chino, inglés simillata yanapayta munanki chayqa, `zh: en` nisqallata qillqayta atinki.

Qhipa kaqtaq [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , mayqinchus sapa simip `README.md` nisqap hatun titulunwan ñawpaq subtítulonwan chawpipi kaqninta hurqun `README.md` qillqasqata paqarichinanpaq. Códigoqa ancha sasan, qam kikiyki qhawayta atinki.

Google API llamk'achkan mana qullqiyuq tikraypaq. Sichus mana Googleman yaykuyta atikunkichu, ama hina kaspa huk proxyta ruway chaymanta churay, kayhina:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Tikray qillqa mayt'uqa `.i18n` willañiqipi tikrasqa waqaychasqatam paqarichinqa, ama hina kaspa `git status` qhaway, chaymantataq k'iti waqaychanaman yapay, mana kuti t'ikraykunata ruwanaykipaq.

Ama hina kaspa, `bunx i18n` sapa kuti tikrayta hukchaspa purichiy, waqaychasqa musuqchaypaq.

Sichus ñawpaq qillqa chaymanta tikray huk pachallapi hukchasqa kanku, waqaychasqa pantasqa kanqa, chayrayku sichus hukchayta munanki, huklla tikrayta atikunki, chaymanta `bunx i18n` purichiy waqaychasqa musuqyachiypaq.
