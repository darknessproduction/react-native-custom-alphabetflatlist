# react-native-custom-alphabetflatlist

A Flatlist with alphabet sidebar.
When the list doesnt have items with letter you pressed on, onPressLetterWithNoMatches is called
    this.props.onPressLetterWithNoMatches
After the list is scrolled to items with letter you pressed on, onPressLetter is called
    this.props.onPressLetter

## Usage

```
    import AlphabetFlatList from 'react-native-custom-alphabetflatlist'

    /* inside your render function */
    <AlphabetFlatList
        renderItem={this.renderItem}
        data={names}
        getItemLayout={this.getItemLayout}
        />
```

## Example

Please check the [example](https://github.com/darknessproduction/react-native-custom-alphabetflatlist/blob/master/example/AlphabetFlatListExample.js) folder.

![](https://github.com/darknessproduction/react-native-custom-alphabetflatlist/blob/master/example/demo.gif)

## Props

You can use all the props provided by FlatList.

| Name                       | Type     | Default                                                                                                                                                                                             | Required | Description                                                                                                                                                                            |
| -------------------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| data                       | array    |                                                                                                                                                                                                     | YES      | Expects array of strings. If you are passing array of objects then also use matchFieldName prop.                                                                                       |
| renderItem                 | function |                                                                                                                                                                                                     | YES      |
| keyExtractor               | function | (item, index) => index.toString()                                                                                                                                                                   |          |
| viewabilityConfig          | object   | { itemVisiblePercentThreshold: 50 }                                                                                                                                                                 |          |
| getItemLayout              | function |                                                                                                                                                                                                     | YES      |
| mainFlatListContainerStyle | object   | {}                                                                                                                                                                                                  |          |
| alphabetListProps          | object   | { <br>&ensp;alphabetListContainerStyle: {},<br>&ensp;alphabetButtonStyle: {},<br>&ensp;selectedAlphabetButtonStyle: {},<br>&ensp;alphabetTextStyle: {},<br>&ensp;selectedAlphabetTextStyle: {}<br>} |          |
| matchFieldName             | string   | false                                                                                                                                                                                               |          | If data array contains object then pass a field name whose value you want to show on main list. See [Issue #2](https://github.com/darknessproduction/react-native-custom-alphabetflatlist/issues/2). |
