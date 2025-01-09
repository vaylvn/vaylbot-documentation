# Text-to-Speech (TTS) Functionality in Vayl

The Text-to-Speech (TTS) functionality in **Vayl** allows users to integrate dynamic voice interactions into their chatbot. With support for multiple voice packs and customizable parameters, the TTS feature provides a flexible and powerful way to enhance viewer engagement.

---

## Overview of Voice Packs and Voices

Vayl supports multiple TTS voice packs, each with its own set of voices. The bot automatically determines the correct voice pack based on the chosen voice.

### Supported Voice Packs

#### **Cepstral**
- Allison, Amy, Belle, Callie, Charlie, Dallas, Damien, David, Diane, Duchess, Emily, Linda, Robin, Shouty, Walter, William, Whispery, Lawrence, Millie, Duncan, Vittoria, Katrin, Matthias, Isabelle, Jean-Pierre, Alejandra, Miguel

#### **IBM Watson**
- en-GB_CharlotteV3Voice, en-GB_JamesV3Voice, en-GB_KateV3Voice, en-AU_JackExpressive, en-AU_HeidiExpressive, en-US_AllisonV3Voice, en-US_AllisonExpressive, en-US_EmilyV3Voice, en-US_EmmaExpressive, en-US_HenryV3Voice, en-US_KevinV3Voice, en-US_LisaV3Voice, en-US_LisaExpressive, en-US_MichaelV3Voice, en-US_MichaelExpressive, en-US_OliviaV3Voice, nl-NL_MerelV3Voice, fr-FR_NicolasV3Voice, fr-FR_ReneeV3Voice, fr-CA_LouiseV3Voice, de-DE_BirgitV3Voice, de-DE_DieterV3Voice, de-DE_ErikaV3Voice, it-IT_FrancescaV3Voice, ja-JP_EmiV3Voice, ko-KR_JinV3Voice, pt-BR_IsabelaV3Voice, es-ES_EnriqueV3Voice, es-ES_LauraV3Voice, es-LA_SofiaV3Voice, es-US_SofiaV3Voice

#### **Oddcast**
- 4-3-1, 6-2-1, 5-4-1, 4-2-1, 5-3-1, 2-7-1, 1-7-1, 7-4-1, 5-2-1, 12-4-1, 8-4-1, 9-2-1, 10-2-1, 4-7-1, 4-4-1, 10-4-1, 3-7-1, 13-4-1, 5-7-1, 6-7-1, 9-4-1, 11-2-1, 7-2-1, 6-3-1, 8-3-1, 7-7-1, 3-1-1, 1-1-1, 2-2-1, 7-3-1, 2-4-1, 3-3-1, 1-3-1, 2-1-1, 2-3-1, 4-1-1, 11-4-1, 8-2-1, 1-2-1, 3-4-1, 8-7-1, 1-7-27, 2-7-27, 2-2-27, 1-4-27, 1-2-27, 1-4-22, 3-2-5, 2-2-5, 1-2-5, 1-4-5, 3-3-10, 5-3-10, 4-3-10, 1-2-10, 2-2-10, 4-4-10, 4-7-10, 6-3-10, 7-3-10, 1-4-10, 3-7-10, 2-7-10, 1-7-10, 2-4-10, 8-3-10, 1-7-18, 1-4-18, 1-7-19, 2-7-19, 1-2-19, 1-4-19, 2-2-19, 2-4-11, 2-7-11, 1-7-11, 2-2-11, 1-2-11, 4-4-11, 1-4-11, 1-2-31, 2-7-32, 1-7-32, 2-2-23, 1-4-23, 1-2-23, 1-7-23, 2-1-4, 2-7-4, 1-7-4, 2-2-4, 4-2-4, 3-2-4, 1-1-4, 4-3-4, 3-3-4, 3-4-4, 5-4-4, 4-4-4, 5-2-4, 1-3-4, 1-4-4, 4-7-4, 2-4-4, 2-3-4, 3-7-4, 6-2-4, 3-1-4, 1-2-15, 3-4-3, 2-7-3, 1-7-3, 3-2-3, 1-1-3, 1-3-3, 2-1-3, 2-2-3, 1-4-3, 2-3-3, 2-4-3, 1-2-8, 1-4-8, 1-7-8, 2-7-8, 3-2-8, 2-7-24, 1-4-24, 1-7-24, 1-4-29, 1-7-29, 2-7-28, 1-4-28, 1-7-28, 2-7-7, 1-7-7, 1-3-7, 10-2-7, 9-2-7, 5-2-7, 6-2-7, 8-2-7, 1-2-7, 1-4-7, 7-2-7, 2-3-7, 2-2-7, 2-4-7, 3-2-7, 6-3-12, 5-3-12, 1-7-12, 2-7-12, 1-4-12, 3-3-12, 7-3-12, 4-3-12, 2-3-12, 8-3-12, 7-3-13, 4-3-13, 8-3-13, 10-3-13, 5-3-13, 2-3-13, 1-4-13, 6-3-13, 1-3-13, 9-3-13, 1-7-20, 2-2-20, 2-7-20, 2-4-20, 1-2-20, 1-4-14, 1-7-14, 2-2-14, 2-7-14, 1-2-14, 2-7-6, 3-4-6, 3-7-6, 4-7-6, 1-7-6, 1-3-6, 2-3-6, 2-4-6, 1-2-30, 1-4-30, 2-2-21, 2-4-21, 1-2-21, 1-7-37, 3-4-37, 1-2-2, 6-2-2, 2-2-2, 9-2-2, 4-3-2, 5-3-2, 1-4-2, 3-4-2, 7-2-2, 8-2-2, 10-2-2, 4-2-2, 3-2-2, 2-1-2, 5-2-2, 2-3-2, 3-3-2, 5-4-2, 4-4-2, 1-1-2, 1-3-2, 1-4-9, 1-2-9, 1-7-9, 2-7-9, 3-4-9, 2-2-9, 1-4-26, 1-3-26, 2-3-26, 1-4-16, 2-7-16, 1-2-16, 3-2-16, 1-7-16, 2-2-16, 1-7-40

#### **StreamElements**
- Brian, Amy, Emma, Geraint, Russell, Nicole, Joey, Justin, Matthew, Ivy, Joanna, Kendra, Kimberly, Salli, Raveena, Zhiyu, Mads, Naja, Ruben, Lotte, Mathieu, Celine, Chantal, Hans, Marlene, Vicki, Aditi, Karl, Dora, Carla, Bianca, Giorgio, Takumi, Mizuki, Seoyeon, Liv, Ewa, Maja, Jacek, Jan, Ricardo, Vitoria, Cristiano, Ines, Carmen, Maxim, Tatyana, Enrique, Conchita, Mia, Miguel, Penelope, Astrid, Filiz, Gwyneth, en-US-Wavenet-A, en-US-Wavenet-B, en-US-Wavenet-C, en-US-Wavenet-D, en-US-Wavenet-E, en-US-Wavenet-F, en-US-Standard-B, en-US-Standard-C, en-US-Standard-D, en-US-Standard-E, en-GB-Standard-A, en-GB-Standard-B, en-GB-Standard-C, en-GB-Standard-D, en-GB-Wavenet-A, en-GB-Wavenet-B, en-GB-Wavenet-C, en-GB-Wavenet-D, en-AU-Standard-A, en-AU-Standard-B, en-AU-Wavenet-A, en-AU-Wavenet-B, en-AU-Wavenet-C, en-AU-Wavenet-D, en-AU-Standard-C, en-AU-Standard-D, en-IN-Wavenet-A, en-IN-Wavenet-B, en-IN-Wavenet-C, af-ZA-Standard-A, ar-XA-Wavenet-A, ar-XA-Wavenet-B, ar-XA-Wavenet-C, bg-bg-Standard-A, cmn-CN-Wavenet-A, cmn-CN-Wavenet-B, cmn-CN-Wavenet-C, cmn-CN-Wavenet-D, cs-CZ-Wavenet-A, da-DK-Wavenet-A, nl-NL-Standard-A, nl-NL-Wavenet-A, nl-NL-Wavenet-B, nl-NL-Wavenet-C, nl-NL-Wavenet-D, nl-NL-Wavenet-E, fil-PH-Wavenet-A, fi-FI-Wavenet-A, fr-FR-Standard-C, fr-FR-Standard-D, fr-FR-Wavenet-A, fr-FR-Wavenet-B, fr-FR-Wavenet-C, fr-FR-Wavenet-D, fr-CA-Standard-A, fr-CA-Standard-B, fr-CA-Standard-C, fr-CA-Standard-D, de-DE-Standard-A, de-DE-Standard-B, de-DE-Wavenet-A, de-DE-Wavenet-B, de-DE-Wavenet-C, de-DE-Wavenet-D, el-GR-Wavenet-A, hi-IN-Wavenet-A, hi-IN-Wavenet-B, hi-IN-Wavenet-C, hu-HU-Wavenet-A, is-is-Standard-A, id-ID-Wavenet-A, id-ID-Wavenet-B, id-ID-Wavenet-C, it-IT-Standard-A, it-IT-Wavenet-A, it-IT-Wavenet-B, it-IT-Wavenet-C, it-IT-Wavenet-D, ja-JP-Standard-A, ja-JP-Wavenet-A, ja-JP-Wavenet-B, ja-JP-Wavenet-C, ja-JP-Wavenet-D, ko-KR-Standard-A, ko-KR-Wavenet-A, lv-lv-Standard-A, nb-no-Wavenet-E, nb-no-Wavenet-A, nb-no-Wavenet-B, nb-no-Wavenet-C, nb-no-Wavenet-D, pl-PL-Wavenet-A, pl-PL-Wavenet-B, pl-PL-Wavenet-C, pl-PL-Wavenet-D, pt-PT-Wavenet-A, pt-PT-Wavenet-B, pt-PT-Wavenet-C, pt-PT-Wavenet-D, pt-BR-Standard-A, ru-RU-Wavenet-A, ru-RU-Wavenet-B, ru-RU-Wavenet-C, ru-RU-Wavenet-D, sr-rs-Standard-A, sk-SK-Wavenet-A, es-ES-Standard-A, sv-SE-Standard-A, tr-TR-Standard-A, tr-TR-Wavenet-A, tr-TR-Wavenet-B, tr-TR-Wavenet-C, tr-TR-Wavenet-D, tr-TR-Wavenet-E, uk-UA-Wavenet-A, vi-VN-Wavenet-A, vi-VN-Wavenet-B, vi-VN-Wavenet-C, vi-VN-Wavenet-D, Linda, Heather, Sean, Hoda, Naayf, Ivan, Herena, Tracy, Danny, Huihui, Yaoyao, Kangkang, HanHan, Zhiwei, Matej, Jakub, Guillaume, Michael, Karsten, Stefanos, Szabolcs, Andika, Heidi, Kalpana, Hemant, Rizwan, Filip, Lado, Valluvar, Pattara, An

#### **Streamlabs**
- Brian, Amy, Emma, Geraint, Russell, Nicole, Joey, Justin, Matthew, Ivy, Joanna, Kendra, Kimberly, Salli, Raveena, Zeina, Zhiyu, Mads, Naja, Ruben, Lotte, Mathieu, Celine, Lea, Chantal, Hans, Marlene, Vicki, Aditi, Karl, Dora, Carla, Bianca, Giorgio, Takumi, Mizuki, Seoyeon, Liv, Ewa, Maja, Jacek, Jan, Ricardo, Camila, Vitoria, Cristiano, Ines, Carmen, Maxim, Tatyana, Enrique, Conchita, Lucia, Mia, Miguel, Lupe, Penelope, Astrid, Filiz, Gwyneth

#### **VoiceForge**
- Conrad, Designer, Diesel, Dog, Evilgenius, Frank, French-fry, Gregory, Jerkface, JerseyGirl, Kayla, Kevin, Kidaroo, Princess, RansomNote, Robot, Shygirl, Susan, Tamika, TopHat, Vixen, Vlad, Warren, Wiseguy, Zach, Obama

---

## Syntax for Using TTS

To trigger the TTS functionality, use the following command format:

```yaml
tts ; voice ; message ; halt ; limit
```

### Parameters

1. **Voice**:
   - Specifies the voice to use for TTS.
   - The bot automatically determines the corresponding voice pack based on the voice name.

2. **Message**:
   - The text to be spoken by the TTS.
   - Supports variable tags (e.g., `[counter:name]`, `[text:name]`, etc.).
   - Users can also utilize the `pronunciation.yml` file in the configuration folder to define custom pronunciations for specific words (e.g., usernames).

3. **Halt**:
   - A boolean (`true` or `false`) that specifies whether Vayl should wait for the TTS to finish speaking before executing further actions in the action list.

4. **Limit**:
   - Specifies the maximum character length for the message.
   - If the message exceeds this limit, the TTS action will be skipped.

---

## Customizing Pronunciations

To ensure proper pronunciation of specific words, such as usernames, you can use the `pronunciation.yml` file located in the configuration folder. This file allows you to map words to their phonetic equivalents.

### Example: `pronunciation.yml`
```yaml
valonvn: valon vee n
swdofberserk: sword of berserk
```

When Vayl encounters these words in the TTS message, it will use the specified pronunciation.

---

## Examples

### Basic Example

```yaml
actions:
- tts ; Brian ; Hello, [ruser]! Welcome to the stream! ; true ; 200
```

- **Voice**: `Brian`
- **Message**: "Hello, [ruser]! Welcome to the stream!"
- **Halt**: `true` (waits for TTS to finish before proceeding).
- **Limit**: `200` characters.

### Example with Custom Pronunciations

```yaml
actions:
- tts ; Amy ; Thank you, JohnDoe, for the sub! ; false ; 150
```

- Uses the pronunciation defined in `pronunciation.yml` to correctly say "John Doe."

### Skipping Long Messages

```yaml
actions:
- tts ; Emma ; This is a really long message that exceeds the character limit and will not be spoken. ; true ; 50
```

- Message length exceeds the `50`-character limit, so the TTS action will be skipped.

---

## Best Practices
- Choose appropriate voices to fit the tone of your stream.
- Define pronunciations for custom terms using `pronunciation.yml`.
- Test different voice packs to find the best fit for your audience.
- Keep message lengths concise to maintain flow.

