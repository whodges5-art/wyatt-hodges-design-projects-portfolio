# A4 – Motor Mount.

## Objective
Use parametric design to model a motor mount in CAD. 

## Analyze
![Problem](A4Problem.png)

![Motor](A4Motor.png)

For this assignment we are tasked with creating a motor mount that is made of two features one that connects to a wall and another that connects to a Brushed 24V DC Gear Motor 3.6Kg.cm/46RPM w/ 99.5:1 Planetary Gearbox (dimensions shown above). The feature with the motor attached will have a force applied that cannot exceed to material max stress and cannot cause the feature to deflect more than 0.30 mm. The material can be PLA, ABS, or PETG

In order to research motor mounts I googled "mounting bracket gearbox motor mount designs" and found a lot of images that gave good layout for my design.

![Examples](A4Examples.png)

## Decide

For this assignment I chose PLA as the material because it is cheapest and should suffice as a support material. When I followed the given link to [MatWeb](https://www.matweb.com/search/DataSheet.aspx?MatGUID=ab96a4c0655c4018a8785ac4031b9278&ckck=1) I found the flexural yield strength is equal to 79-93 MPa and a flexural modulus equal to 2.96-3.6 GPa. I will use the smaller values when modeling because I need to find min cross-sectional area necessary and smaller strength and modulus will will produce larger values.

## Communicate

### Figure 1


### Appendix 
[Example Mounts](https://www.google.com/search?q=mounting+bracket+gearbox+motor+mount+designs&sca_esv=326e45127ec9a721&rlz=1C1VDKB_enUS959US967&udm=2&biw=1536&bih=730&sxsrf=APpeQns8jFo_-obYn5SgVI46MUhmRigk2Q%3A1789612536919&ei=-FGras_dN7G_p84PrNzD-Ak&ved=2ahUKEwjPubGcyvSWAxWx38kDHSzuEJ8Q4dUDegQIBhAN&uact=5&oq=mounting+bracket+gearbox+motor+mount+designs&gs_lp=Egtnd3Mtd2l6LWltZyIsbW91bnRpbmcgYnJhY2tldCBnZWFyYm94IG1vdG9yIG1vdW50IGRlc2lnbnNI0jBQwg5YgC1wAXgAkAEAmAFUoAHuBqoBAjExuAEDyAEA-AEBmAIAoAIAmAMAiAYBkgcAoAeEAbIHALgHAMIHAMgHAIAIAQ&sclient=gws-wiz-img)
