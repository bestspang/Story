# Story
## [Fennect](https://www.fennect.com/)

### Work in progress

**VRf_templateBP VR template based on BP:**

this is `main template`

[https://github.com/bestspang/VRf_templateBP](https://github.com/bestspang/VRf_templateBP)
```
git clone https://github.com/bestspang/VRf_templateBP
```
**Multi-player simple LAN template:**

[https://github.com/bestspang/VRf_templates](https://github.com/bestspang/VRf_templates)
```
git clone https://github.com/bestspang/VRf_templates
```
**VRf_multiplayerV1 3rd person test template:**

[https://github.com/bestspang/VRf_multiplayerV1](https://github.com/bestspang/VRf_multiplayerV1)
```
git clone https://github.com/bestspang/VRf_multiplayerV1
```
__note that all of these are unfinished projects__

## Updates

#### TO DO lists:
1. LAN
2. UI menu
3. Plot_CNN.ipynb

## Processing

**Orbit**

The project is based on `acceleration` and Newton's rules `F=MA`...
```
PVector p1;
PVector p2;
float a;
float b;

void setup() {
  size(400, 400);
  p1 = new PVector(random(200), random(200));
  p2 = new PVector(random(200, 400), random(0, 400));
  PVector sub = PVector.sub(p2, p1);
  // y = a * x + b
  a = sub.y / sub.x;
  b = p1.y - a * p1.x;
  cursor(CROSS);
}

void draw() {
  background(255);
  line(p1.x, p1.y, p2.x, p2.y);
  fill(255);
  ellipse(p1.x, p1.y, 10, 10);
  if ((mouseY > (a * mouseX + b - 0.5)) && (mouseY < (a * mouseX + b + 0.5))) {
    fill(255, 0, 0);
    ellipse(mouseX, mouseY, 20, 20);
  }
}
```
https://forum.processing.org/two/discussion/90/point-and-line-intersection-detection
