# Anki Guide for Japanese Flashcards

Todo: Details about the official Anki and fake ones.

Below are some helpful tips for you to get the most out of your Anki flashcards. Remember that the more work you put into recalling your cards (think: typing your answers), the better you will learn them.

## Table of contents
1. [How to import flashcards into Anki](#how-to-import-flashcards-into-anki)
1. [How to change the Anki deck to enable typing answers](#how-to-change-the-anki-deck-to-enable-typing-answers)
1. [Add a new Note Type for sentences](#add-a-new-note-type-for-sentences)
1. [Type in the gaps cards (using cloze)](#type-in-the-gaps-cards-using-cloze)
    1. [Adding additional fields to your cards](#adding-additional-fields-to-your-cards)
    1. [Type in the gaps cards (using cloze deletion)](#type-in-the-gaps-cards-using-cloze-deletion)
    1. [Add new cards](#add-new-cards)
    1. Furigana - tbd


### How to import flashcards into Anki
Official instructions about shared decks and importing can be found [here](https://docs.ankiweb.net/getting-started.html#shared-decks).

tl;dr; Double click on your downloaded `.apkg` file.

### How to change the Anki deck to enable typing answers

[Official instructions here](https://docs.ankiweb.net/templates/fields.html?highlight=type#checking-your-answer).

I highly recommend that you change any pre-made decks to enable typing in answers.

The following are instructions show editing the deck [Genki 1 3rd edition with sound files](https://ankiweb.net/shared/info/1742947823) to allow typing answers:

1. Click "Browse"
![click browse](./images/Type%20In/1%20Browse.png)
1. With any one of the Genki cards that has the Japanese "Card Type" selected, click "Cards..."
![click cards](./images/Type%20In/2%20Cards.png)
1. On the Japanese card type, add the following to the bottom of the "Front Side" template
    ```
    <br>
    {{type:english}}
    ``` 
    ![edit japanese front side template](./images/Type%20In/3%20Japanese%20Front.png)
    <center><i>Note that &lt;br&gt; is just for adding extra space and is not necessary.</i></center>
1. Change the Card Type to the English card type (Note: you can also select the English version from the "Browse" page)
![select english card type](./images/Type%20In/4%20Select%20English.png)
1. Add the following to the bottom of the English "Front Side" template
    ```
    <br>
    {{type:japanese_kana}}
    ```
    ![edit english front side template](./images/Type%20In/5%20English%20Front.png)
1. Study!
    ![type in your answer](./images/Type%20In/6-1%20Type%20answer.png)
    ![view answer](./images/Type%20In/6-2%20View%20answer.png)

Note: this will not automatically decide if your answer is correct or not. It will highlight how much of your answer matched, but you still must select how well you did (tip: type numbers 1, 2, 3, or 4 to rate yourself).

### Add a new Note Type for sentences
The following new note type is going to be used for adding sentences to practice. It will use [Cloze Deletion](https://docs.ankiweb.net/editing.html#cloze-deletion) to hide the section to fill in, it will allow you to type in your answers, it will include a new field, and it will display Japanese furigana (the little hiragana pronunciation of kanji).

1. 
![](./images//New%20Note%20Type/1%20Manage%20Note%20Types.png)
![](./images//New%20Note%20Type/2%20Add%20new%20Note%20Type.png)
![](./images//New%20Note%20Type/3%20Use%20Add%20Cloze.png)
![](./images//New%20Note%20Type/4%20Name.png)



#### Adding additional fields to your cards
[Official documentation on customising fields](https://docs.ankiweb.net/editing.html#customizing-fields).

In this example, I will show adding a new heading / title field to my cards.

1. Go to the card template for one of the cards in your deck
    1. See [enable typing answers instructions](#how-to-change-the-anki-deck-to-enable-typing-answers) if you are not sure how to get there
1. Add the new 
![](./images/New%20Field/1%20New%20Field.png)
![](./images/New%20Field/2%20Add%20Field.png)
![](./images/New%20Field/3%20Name%20Field.png)

Note: don't make it the first field. The first field cannot be empty and is used to decide if this card is a duplicate or not. It makes most sense to have the Text field as the first one.
![](./images/New%20Field/4%20Reposition.png)
![](./images/New%20Field/5%20Move%20to%20first%20position.png)
![](./images/New%20Field/6%20Repositioned.png)
![](./images/New%20Field/7%20Result%20adding.png)
changing the [Card Template](https://docs.ankiweb.net/templates/intro.html#card-templates)
![](./images/New%20Field/8%20Edit%20cards.png)
![](./images/New%20Field/9%20Plain%20add%20to%20card.png)
![](./images/New%20Field/10%20Add%20for%20style.png)
[Styling](https://docs.ankiweb.net/templates/styling.html) the card template
![](./images/New%20Field/11%20Style%20Field.png)

#### Type in the gaps cards (using cloze deletion)
https://www.youtube.com/watch?v=5tYObQ3ocrw

This is essentially the same as the [enable typing answers instructions](#how-to-change-the-anki-deck-to-enable-typing-answers) above, but with slightly different syntax for the cloze.

Note, the field in which you will type the cloze is called "Text".

1. From the Card editor (see above), add a field for typing your answer for the cloze at the bottom of the Front Template:
    ```
    <br>
    <br>
    {{type:cloze:Text}}
    ```
    ![Edit front template](./images/Type%20in%20cloze/1%20Front%20template.png)
1. On the Back Template add a field showing a comparison of your answer to the actual answer. I added the following in between the Text field and the Back Extra field:
    ```
    <br>
    <br>
    {{type:cloze:Text}}
    <br>
    <br>
    ```
    ![Edit back template](./images/Type%20in%20cloze/2%20Back%20template.png)
1. Done!

### Add new cards
![](./images/Add%20New%20Card/1%20Add.png)
![](./images/Add%20New%20Card/2%20Select%20Type%20and%20Deck.png)
![](./images/Add%20New%20Card/3%20Fill%20out%20fields.png)
![](./images/Add%20New%20Card/4%20Select%20and%20cloze.png)
![](./images/Add%20New%20Card/5%20Cloze%20result.png)
![](./images/Add%20New%20Card/6%20All%20clozed.png)
![](./images/Add%20New%20Card/7%20Different%20clozes.png)
![](./images/Add%20New%20Card/8%20Add.png)
![](./images/Add%20New%20Card/9%20Study.png)
![](./images/Add%20New%20Card/10%20Study%20answer.png)

### Use Furigana
https://www.youtube.com/watch?v=crNvnR1lKtc