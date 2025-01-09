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
- Various numbered voices such as 4-3-1, 6-2-1, 5-4-1, and more.

#### **StreamElements**
- Brian, Amy, Emma, Geraint, Russell, Nicole, Joey, Justin, Matthew, Ivy, Joanna, Kendra, Kimberly, Salli, Raveena, Zhiyu, Mads, Naja, Ruben, Lotte, Mathieu, Celine, Chantal, Hans, Marlene, Vicki, Aditi, Karl, Dora, Carla, Bianca, Giorgio, Takumi, Mizuki, Seoyeon, Liv, Ewa, Maja, Jacek, Jan, Ricardo, Vitoria, Cristiano, Ines, Carmen, Maxim, Tatyana, Enrique, Conchita, Mia, Miguel, Penelope, Astrid, Filiz, Gwyneth, and more.

#### **Streamlabs**
- Brian, Amy, Emma, Geraint, Nicole, Joey, Justin, Matthew, Ivy, Joanna, Kendra, Kimberly, Salli, Raveena, Zeina, Zhiyu, Mads, Naja, Ruben, Lotte, Mathieu, Celine, Lea, Chantal, Hans, Marlene, Vicki, Aditi, Karl, Dora, Carla, Bianca, Giorgio, Takumi, Mizuki, Seoyeon, Liv, Ewa, Maja, Jacek, Jan, Ricardo, Camila, Vitoria, Cristiano, Ines, Carmen, Maxim, Tatyana, Enrique, Conchita, Lucia, Mia, Miguel, Lupe, Penelope, Astrid, Filiz, Gwyneth.

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

