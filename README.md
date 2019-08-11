: : s p a c e 0 0 0

![space](https://github.com/nicolasbaez/space000/blob/master/space000.gif)

```processing
void setup() {
  size(512, 256);
  background(0);
  smooth();
}
float radio=height*0.75;
float i=0;
void draw() {
  noStroke();
  fill(0, 0, 0, random(16));
  rect(0, 0, width, height);
  fill(255);
  stroke(random(255), 0, 0, random(255));
  float grueso=32;
  float xx=radio*cos(radians(i))+width*0.5;
  float yy=radio*sin(radians(i))+height*0.5;
  ellipse(xx, yy, grueso, grueso);
  i+=0.5;
  if (i>=360&&i<360*2) {
    saveFrame("gif/space000-######.png");
  }
}
```

