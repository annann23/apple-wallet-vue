<template>
<div>
 <div class="sticky-container" ref="sticky-container">
    <div class="sticky">
      <div class="slide-container" ref="slide-container">
        <div class="wallet-container">
          <div class="slide-title" ref="slTitle"><p>Wallet</p></div>
          <div class="slide wallet-image" ref="slWallet">
            <img src="../assets/image/icon_wallet_bg.png" class="wallet-bg">
            <span ref="slCard1" class="card card-1"></span>
            <span ref="slCard2" class="card card-2"></span>
            <span ref="slCard3" class="card card-3"></span>
            <span ref="slCard4" class="card card-4"></span>
            <img src="../assets/image/icon_wallet_bottom.png" class="wallet-bottom">
          </div>
        </div>
        <div class="title-container" ref="titleContainer">
          <div class="title">Carry one thing. <br>Everything.</div>
            <p>
              The Wallet app lives right on your iPhone. 
              It’s where you securely keep your credit and debit cards, 
              driver’s license or state ID, transit cards, event tickets,
              keys, and more — all in one place. And it all works with iPhone 
              or Apple Watch, so you can take less with you but always bring more.
            </p>
            <div class="add-btn">Add a card</div>
        </div>
      </div>
    </div>
  </div>
  <div class="sticky-container-2">
    <div class="sticky-2">
      <div class="slide-container">
        <span  class="card card-1"></span>
        <span  class="card card-2"></span>
        <span  class="card card-3"></span>
        <span  class="card card-4"></span>
      </div>
    </div>
  </div>
</div>

</template>

<script>
import BezierEasing from 'bezier-easing';

const ease =  BezierEasing(0.25, 0.1, 0.25, 1.0);
const midSlow = BezierEasing(0, 0.7, 1, 0.3);

const  def = {
        height: 2100,
        elements: { 
          slTitle:{
            top: 500, 
            bottom: 2000,
            topStyle: {
              translateY: 0,
            },
            bottomStyle: {
              translateY: -1000,
            }
          },
          slWallet: { 
            top: 500, 
            bottom: 2000,
            topStyle: {
              width: 200,
              translateY: 0,
            },
            bottomStyle: {
              width: document.body.clientWidth,
              translateY: 2700,
            }
          },
          slCard1: { 
            top: 500, 
            bottom: 2000,
            topStyle: {
              width: document.body.clientWidth*0.7,
              translateY: 0,
            },
            bottomStyle: {
              width:  document.body.clientWidth*0.7,
              translateY: -100,
            }
          },
          slCard2: { 
            top: 500, 
            bottom: 2000,
            topStyle: {
              width: document.body.clientWidth*0.7,
              translateY: 0,
            },
            bottomStyle: {
              width:  document.body.clientWidth*0.7,
              translateY: -200,
            }
          },
          slCard3: { 
            top: 500, 
            bottom: 2000,
            topStyle: {
              width: document.body.clientWidth*0.7,
              translateY: 0,
            },
            bottomStyle: {
              width:  document.body.clientWidth*0.7,
              translateY: -300,
            }
          },
          slCard4: { 
            top: 500, 
            bottom: 2000,
            topStyle: {
              width: document.body.clientWidth*0.7,
              translateY: 0,
            },
            bottomStyle: {
              width:  document.body.clientWidth*0.7,
              translateY: -400,
            }
          },
          titleContainer: { 
            top: 1200, 
            bottom: 3000,
            topStyle: {
              translateY: 100,
            },
            bottomStyle: {
              translateY: -1500,
            }
          },
        },
        animations: {
          slTitle:[
             {
              top: 500, 
              bottom: 2000,
              easing: ease, 
              styles: { 
                translateY: {
                  topValue: 0, 
                  bottomValue: -1000 
                }
              }
            },
          ],
          slWallet: [
            {
              top: 1500, 
              bottom: 2000,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue: 0, 
                  bottomValue: 2700 
                }
              }
            },
            {
              top: 500,
              bottom: 1500,
              easing: ease,
              styles: {
                width: {
                  topValue: 200,
                  bottomValue: document.body.clientWidth
                }
              }
            },
          ],
          slCard1: [
            {
              top: 1500, 
              bottom: 1600,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue: 0, 
                  bottomValue: -800 
                }
              }
            },
            {
              top: 1600, 
              bottom: 2000,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue:  -800, 
                  bottomValue: -100 
                }
              }
            },
            {
              top: 500,
              bottom: 1500,
              easing: ease,
              styles: {
                width: {
                  topValue: 200*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
            {
              top: 1500,
              bottom: 2000,
              easing: ease,
              styles: {
                width: {
                  topValue: document.body.clientWidth*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
          ],
          slCard2: [
           {
               top: 1500, 
              bottom: 1600,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue: 0, 
                  bottomValue: -800 
                }
              }
            },
            {
              top: 1600, 
              bottom: 2000,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue: -800, 
                  bottomValue: -200 
                }
              }
            },
            {
              top: 500,
              bottom: 1500,
              easing: ease,
              styles: {
                width: {
                  topValue: 200*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
            {
              top: 1500,
              bottom: 2000,
              easing: ease,
              styles: {
                width: {
                  topValue: document.body.clientWidth*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
          ],
          slCard3: [
          {
              top: 1500, 
              bottom: 1600,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue: 0, 
                  bottomValue: -800 
                }
              }
            },
            {
              top: 1600, 
              bottom: 2000,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue:  -800, 
                  bottomValue: -300 
                }
              }
            },
            {
              top: 500,
              bottom: 1500,
              easing: ease,
              styles: {
                width: {
                  topValue: 200*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
            {
              top: 1500,
              bottom: 2000,
              easing: ease,
              styles: {
                width: {
                  topValue: document.body.clientWidth*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
          ],
          slCard4: [
           {
              top: 1500, 
              bottom: 1600,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue: 0, 
                  bottomValue: -800 
                }
              }
            },
            {
              top: 1600, 
              bottom: 2000,
              easing: midSlow, 
              styles: { 
                translateY: {
                  topValue:  -800, 
                  bottomValue: -400 
                }
              }
            },
            {
              top: 500,
              bottom: 1500,
              easing: ease,
              styles: {
                width: {
                  topValue: 200*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
            {
              top: 1500,
              bottom: 2000,
              easing: ease,
              styles: {
                width: {
                  topValue: document.body.clientWidth*0.7,
                  bottomValue: document.body.clientWidth*0.7
                }
              }
            },
          ],
          titleContainer:[
             {
              top: 1200, 
              bottom: 3000,
              easing: ease, 
              styles: { 
                translateY: {
                  topValue: 100, 
                  bottomValue: -1500 
                }
              }
            },
          ],
        }
      };

    const isAmong = (num, top, bottom) => num >= top && num <= bottom;

    const applyStyle = (element, styleName, value, unit = "px") => {
      if (styleName === "translateY") {
        // eslint-disable-next-line no-param-reassign
        element.style.transform = `translateY(${value}${unit})`;
        return;
      }
      // eslint-disable-next-line no-param-reassign
      element.style[styleName] = `${value}${unit}`;
    };

   const enabled = new Map();
   const disabled = new Map();

export default {
  mounted(){
    window.addEventListener("scroll", this.onScroll);
    this.initAnimation();
  },

  beforeDestroy(){
    window.removeEventListener("scroll", this.onScroll);
  },

  methods:{
    applyStyles(currentPos, refname, styles, r, unit = "px") {
      for (const style of Object.keys(styles)) {
        const { topValue, bottomValue } = styles[style];
        const calc = (bottomValue - topValue) * r  + topValue;
        applyStyle(this.$refs[refname], style, calc, unit);
      }
    },

    applyAllAnimation(currentPos, refname) {
      const animations = def.animations[refname];
      if (!animations) return;
      for (const animation of animations) {
        const { top: a_top, bottom: a_bottom, easing, styles } = animation;
        const isIn = isAmong(currentPos, a_top, a_bottom);

        if (isIn) {
          if (!animation.enabled) animation.enabled = true;
        } else if (!isIn && animation.enabled) {
          if (currentPos <= a_top) {
            this.applyStyles(currentPos, refname, styles, 0);
          } else if (currentPos >= a_bottom) {
            this.applyStyles(currentPos, refname, styles, 1);
          }
          // eslint-disable-next-line no-param-reassign
          animation.enabled = false;
        }

        if (animation.enabled) {
          const r = easing((currentPos - a_top) / (a_bottom - a_top));
          // eslint-disable-next-line no-param-reassign
          this.applyStyles(currentPos, refname, styles, r);
        }
      }
    },

    initAnimation() {
      this.$refs["sticky-container"].style.height = `${def.height}px`;

      disabled.clear();
      enabled.clear();

      for (const refname of Object.keys(def.elements)) {
        disabled.set(refname, def.elements[refname]);
      }

      for (const refname of Object.keys(def.animations)) {
        for (const animation of def.animations[refname]) {
          animation.enabled = false;
        }
      }

      disabled.forEach((obj, refname) => {
        Object.keys(obj.topStyle).forEach((styleName) => {
          const pushValue = obj.topStyle[styleName];
          this.$refs[refname].style[styleName] = pushValue;
        });
      });

      this.onScroll();
    },

    onScroll() {
      const scrollTop = window.scrollY || window.pageYOffset;
      const currentPos = scrollTop + window.innerHeight / 2;

      // disabled 순회하며 활성화할 요소 찾기.
      disabled.forEach((obj, refname) => {
        if (
          isAmong(currentPos, obj.top, obj.bottom)
        ) {
          enabled.set(refname, obj);
          this.$refs[refname].classList.remove("disabled");
          this.$refs[refname].classList.add("enabled");
          disabled.delete(refname);
        }
      });

      // enabled 순회하면서 헤제할 요소를 체크
      enabled.forEach((obj, refname) => {
        const { top, bottom, topStyle, bottomStyle } = obj;
        if (!isAmong(currentPos, top, bottom)) {
          // 위로 나갔다면 시작하는 스타일 적용
          if (currentPos <= top) {
            Object.keys(topStyle).forEach((styleName) => {
              applyStyle(this.$refs[refname], styleName, topStyle[styleName]);
            });
          }
          // 아래로 나갔다면 끝나는 스타일적용
          else if (currentPos >= bottom) {
            Object.keys(bottomStyle).forEach((styleName) => {
              applyStyle(
                this.$refs[refname],
                styleName,
                bottomStyle[styleName]
              );
            });
          }

          disabled.set(refname, obj);
          this.$refs[refname].classList.remove("enabled");
          this.$refs[refname].classList.add("disabled");
          enabled.delete(refname);
        }
        
        // enable 순회중, 범위 내부에 제대로 있다면 각 애니메이션 적용시키기.
        else {
          this.applyAllAnimation(currentPos, refname);
        }
      });
    }
  },
}
</script>

<style>
.sticky{
  position: sticky;
  background-color: #d9d6cc;
  top: 0px;
  width: 100%;
  height: 100vh;
  z-index: auto;
}

.slide-container{
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide-title{
  font-size: 240px;
  color: #1d1d1f;
  font-weight: bold;
  letter-spacing: -7px;
  line-height: 0.1;
  display: block;
}

.slide-title p{
  margin: 100px;
}

.wallet-image{
  position: relative;
  display: none;
  z-index: 99;
}

.wallet-image.enabled{
  display: inline-block;
}

.wallet-image img{
  width: 100%;
  height: auto;
  bottom: 0;
  left: 0;
}

.wallet-image img.wallet-bg{
  z-index: 0;
}

.wallet-image .card{
  display: block;
  position: absolute;
  border-radius: 3%/7%;
  width: 70%;
  height: 30%;
  left: 15%;
  z-index: 1;
  box-shadow: 0px -3px 5px rgba(0,0,0,0.2);
}

.wallet-image .card-1{
  top: 26%;
  background-color: #3295c9;
}
.wallet-image .card-2{
  top: 31%;
  z-index: 2;
  background-color: #fcad00;
}
.wallet-image .card-3{
  top: 36%;
  z-index: 3;
  background-color: #50be3d;
}
.wallet-image .card-4{
  top: 41%;
  z-index: 4;
  background-color: #f26d5f;
}

.wallet-image img.wallet-bottom{
  position: absolute;
  bottom: 0;
  z-index: 5;
}

.title-container{
  position: absolute;
  display: block;
  z-index: -1;
  top: 100%;
  width: 100%;
  text-align: center;
}

.title{
  position: relative;
  font-size: 90px;
  font-weight: bold;
  color: #1d1d1f;
  letter-spacing: -5px;
  line-height: 1;
  text-align: center;
  z-index: 999;
}

.title-container p{
  width: 608px;
  margin: 30px auto;
  font-size: 28px;
  font-weight: 600;
  line-height: 1.1;
}

.title-container .add-btn{
  background-color: #1d1d1f;
  width: 130px;
  height: 50px;
  border-radius: 50px;
  color: #fff;
  font-weight: bold;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: center;
}


.sticky-2{
  position: sticky;
  background-color: #d9d6cc;
  top: 0px;
  width: 100%;
  height: 100vh;
  z-index: -1;
}


.sticky-2 .slide-container{
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.sticky-2 .card{
  display: block;
  position: absolute;
  border-radius: 3%/7%;
  width: 70%;
  height: 30%;
  left: 15%;
  z-index: 1;
  box-shadow: 0px -3px 5px rgba(0,0,0,0.2);
}



.sticky-2 .card-1{
  top: 0px;
  background-color: #3295c9;
}
.sticky-2 .card-2{
  top: 30px;
  z-index: 2;
  background-color: #fcad00;
}
.sticky-2 .card-3{
   top: 60px;
  z-index: 3;
  background-color: #50be3d;
}
.sticky-2 .card-4{
  top: 90px;
  z-index: 4;
  background-color: #f26d5f;
}

</style>
