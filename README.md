# Build an iPhone Calculator using React! [2020] 
https://www.youtube.com/watch?v=wOENJWPu23U&ab_channel=JustinKim

https://github.com/angle943/iphone-calculator


## Layout
```
App
  top
  display
  buttons
  bottom
```


## Grid layout
```
.buttons {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(5, 1fr);
}
```
the unit fr stands for fractinal unit, and repeat 1fr N times

```
.Button.zero {
  grid-column: 1 / span 2;
}
set element on the column 1 and span two columns
```
## Dynamic css for the buttons
```
  <div className={`Button ${content === "0" ? "zero" : ""} ${type || ""}`}>
      {content}
  </div>