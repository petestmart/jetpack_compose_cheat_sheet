# jetpack_compose_cheat_sheet
Notes on Jetpack Compose.  These are my personal notes.  Use them if you want.

## Column
### Modifiers
```modifier = Modifier
  .padding(horizontal = 8.dp, vertical = 8.dp),
or use:   (top = 8.dp, bottom = 8.dp, start = 8.dp, end = 8.dp),
```
*GOTCHA* These padding modifiers cannot be mixed and matched
- use horizontal and vertical OR use top, bottom, start, end

### Spacing 
```
horizontalAlignment = Alignment.CenterHorizontally,
```
*GOTCHA* Alignment vs Arrangement
- Watch where you use these two
-`Column`s use `VerticalArrangement` and `HorizontalAlignment`
-`Row`s use `HorizontalArrangement` and `VerticalAlignment`

## Row
### Modifiers
```modifier = Modifier
    .padding(horizontal = 8.dp, vertical = 8.dp),
or use: (top = 8.dp, bottom = 8.dp, start = 8.dp, end = 8.dp),
```
*GOTCHA* These padding modifiers cannot be mixed and matched
- use horizontal and vertical OR use top, bottom, start, end

`horizontalArrangement=`

<img width="489" alt="graphic of the different affects of different uses for arrangement in jetpack compose" src="https://user-images.githubusercontent.com/47460632/171457784-50f960bf-9df1-4555-ae86-79c6dcedcf30.png">
[Source: vitor-ramos.medium.com](https://vitor-ramos.medium.com/understand-arrangement-and-alignment-in-jetpack-compose-7633f2ed5b39)

## Box
``` 
Box(
   modifier = Modifier
       .size(
           width = 28.dp,
           height = 14.dp,
       )
       .fillMaxWidth(.85f <- Enter Float Value as Percentage) <- This parameter would be used in place of .size
       .background(color = Color.LightGray)
)
```
## Card
*GOTCHA* Card vs Box
- Cards have a shape parameter.  Boxes do not.

## Canvas
```
Canvas (
	modifier = Modifier
	onDraw = { // this: DrawScope
		// Basic Circle
		drawCircle (
			color = Color.LightGray,
			center = Offset( //x value, //y value), <- Float Values
			radius = size.width / 2,
		)
		// Basic Line
		drawLine (
			color = Color.LightGray,
			start = Offset( //x value, //y value), <- Float Values
			end = Offset(size.width, 0f), <- Example Values
		)
		// Basic Rectangle
		drawRect(
			color = Color.LightGray,
			topLeft = Offset((size.width * .25, 0f),
			size = Size(size.width *.15f, size.width * 15f),
		)
	}
)
```
