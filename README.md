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
