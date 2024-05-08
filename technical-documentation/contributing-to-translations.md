# Contributing to translations

{% hint style="warning" %}
Follow the linked guide first to set up the project.
{% endhint %}

{% content-ref url="build-guide/" %}
[build-guide](build-guide/)
{% endcontent-ref %}

***

{% hint style="danger" %}
Be sure to create the new file while using(checked out) the DEV branch, not MASTER.
{% endhint %}

Duplicate the en.json and adjust its file name according to the wanted language code, e.g. da.json (Danish)

{% embed url="https://github.com/tiltedphoques/TiltedEvolution/blob/master/Code/skyrim_ui/src/assets/i18n/en.json" %}

{% hint style="info" %}
You can find the language codes on this page or by using google e.g. "danish language code"

[http://www.lingoes.net/en/translator/langcode.htm](http://www.lingoes.net/en/translator/langcode.htm)
{% endhint %}

Then translate all strings in the file.

{% hint style="danger" %}
Do not change the key words such as the underline and similar coloured in green. ![](../.gitbook/assets/image.png)
{% endhint %}

Further you need to update the following file with the language you've just added

{% embed url="https://github.com/tiltedphoques/TiltedEvolution/blob/dev/Code/skyrim_ui/src/app/transloco-root.module.ts" %}

Below you can see the whole array of languages (it might be outdated).

```typescript
 availableLangs: [
          { id: 'en', label: 'English' },
          { id: 'de', label: 'Deutsch' },
          { id: 'ru', label: 'Русский' },
          { id: 'fr', label: 'Français' },
          { id: 'zh-CN', label: '中文（中国）' },
          { id: 'nl', label: 'Nederlands' },
          { id: 'es', label: 'Español' },
          { id: 'ko', label: '한국어' },
          { id: 'tr', label: 'Türkçe' },
          { id: 'cs', label: 'Čeština' },
          { id: 'pl', label: 'Polski' },
          { id: 'overwrite', label: 'Custom' },
        ],
```

To add your newly added language to the ingame selection, you need to duplicate one of the lines and adjust both the id and the label. Below is an example how the line could look like and how it would look like in the whole array.

```typescript
{ id: 'da', label: 'Dansk' },
```

```typescript
 availableLangs: [
          { id: 'en', label: 'English' },
          { id: 'de', label: 'Deutsch' },
          { id: 'ru', label: 'Русский' },
          { id: 'fr', label: 'Français' },
          { id: 'zh-CN', label: '中文（中国）' },
          { id: 'nl', label: 'Nederlands' },
          { id: 'es', label: 'Español' },
          { id: 'ko', label: '한국어' },
          { id: 'tr', label: 'Türkçe' },
          { id: 'cs', label: 'Čeština' },
          { id: 'pl', label: 'Polski' },
          { id: 'da', label: 'Dansk' },
          { id: 'overwrite', label: 'Custom' },
        ],
```

Then create a pull request like [https://github.com/tiltedphoques/TiltedEvolution/pull/671](https://github.com/tiltedphoques/TiltedEvolution/pull/671) with your new localisation file.
