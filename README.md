#Fissure

Fissure adds support for cascading CSS classNames to react-native as they exist in HTML5. Note, does not support multiple classNames yet, but on the TODO list.

## Install
```
npm install fissure
```


## Example

```
var React = require('react-native');
var Fissure = require("fissure");
var {
  AppRegistry,
  StyleSheet,
  Text,
  ScrollView,
  View
} = React;

var feed = React.createClass({

	render: function() {
		return Fissure.render(styles, (
			<ScrollView className="feed" >
				<View className="post">
					<View className="h3">
						<Text className="author">Jon Hamm </Text>
						<Text>shared this</Text>
					</View>
					<Text className="h1">Mad Men Season Premiere Tonight</Text>
					<Text className="h2">theverge.com</Text>
				</View>
			</ScrollView>
		));
	}

});

var styles = StyleSheet.create(Fissure.styles({
	feed : {
		flexDirection: "row",
		margin:30,

		post : {
			h3 : {
				flexDirection: "row",
				fontSize: 8,

				author : {
					color: "#3498db"
				}
			},
			h1 : {
				fontSize: 14,
				fontWeight: "700",
				marginBottom:2	
			},
			h2 : {
				fontSize: 10,
		 		color: "#999",
				marginBottom:2	
			}
		},
	}
}))

module.exports = feed;
```

