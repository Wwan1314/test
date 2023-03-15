<template>
  <div>
    <!-- 头部 -->
    <div class="yl-lab">
      <div class="yl-lab-cont">
        <div><img src="../assets/logo.png" alt="" /></div>
        <ul>
          <li v-for="i in toplist" :key="i">
            <a href="">{{ i }}</a>
          </li>
        </ul>
        <a class="yl-nn" href="">Connect</a>
      </div>
    </div>
    <!-- 展示 -->
    <div class="yl-topall">
      <div class="yl-vo">
        <video autoplay loop muted class="bgvideo" id="bgvideo">
          <source src="../assets/video.webm" type="video/webm" />
        </video>
      </div>
      <div class="yl-text">
        <h1 class="yl-font1">
          THE MOST ADVANCED USDT Machine
          <br />
          BASED ON BINANCE SMARTCHAIN
        </h1>
        <h3 class="yl-font2">
          ENJOY UP TO 16% DAILY REWARDS AND 5,840% ROI
        </h3>
        <div class="yl-showlist">
          <ul>
            <li v-for="i in showlist" :key="i">
              <a style="color: white;" href="">{{ i }}</a>
            </li>
          </ul>
        </div>
        <div class="yl-biao">
          <a href="">
            <svg
              width="64"
              class="go-down"
              height="64"
              viewBox="0 0 64 64"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <rect
                width="64"
                height="64"
                rx="13"
                fill="#48b090"
                fill-opacity="0.16"
              ></rect>
              <path
                d="M39.1328 31.2109C38.7422 30.8203 38.1562 30.8594 37.7656 31.2109L33.3125 35.9375V24.6875C33.3125 24.1797 32.8828 23.75 32.375 23.75H31.125C30.5781 23.75 30.1875 24.1797 30.1875 24.6875V35.9375L25.6953 31.2109C25.3047 30.8594 24.7188 30.8203 24.3281 31.2109L23.4688 32.0703C23.1172 32.4219 23.1172 33.0469 23.4688 33.3984L31.0859 40.9766C31.4375 41.3672 32.0234 41.3672 32.4141 40.9766L39.9922 33.3984C40.3438 33.0469 40.3438 32.4609 39.9922 32.0703L39.1328 31.2109Z"
                fill="white"
              ></path>
            </svg>
          </a>
        </div>
      </div>
    </div>
    <!-- MINING -->
    <div class="yl-min">
      <div class="yl-minbox">
        <h2>MINING</h2>
        <div class="flex mar">
          <div v-for="i in minlist" :key="i" class="yl-mintop flex">
            <img src="../assets/图标.png" alt="" />
            <div class="yl-mintop-text">
              <span>{{ i }}</span>
              <span>?</span>
            </div>
          </div>
        </div>
        <div class="yl-mincont flex">
          <div class="yl-mincont-left">
            <div class="yl-minleft-top">
              <img src="../assets/图标.png" alt="" />
              <div class="yl-mintop-text1">
                <span class="text">0</span>
                <span>MINERS</span>
              </div>
            </div>
            <div class="yl-minleft-t flex">
              <div>
                <h2>DIGGING</h2>
                <p class="yl-minp">
                  <img src="../assets/图标.png" alt="" />
                  ESTIMATED YIELD:
                  <span>?</span>
                  USDT
                </p>
              </div>
              <div class="yl-marg">
                <h2>MINDE</h2>
                <p class="yl-minp">
                  <img src="../assets/图标.png" alt="" />
                  IMNERS:
                  <span>?</span>
                </p>
                <p class="yl-minp">
                  <img src="../assets/图标.png" alt="" />
                  REWARD:
                  <span>?</span>
                  USDT
                </p>
              </div>
            </div>
            <div class="yl-minleft-s">
              <div class="yl-minleft-top">
                <div class="yl-minleft-top-le">
                  <p>WALLET BALANCE</p>
                  <p>0</p>
                </div>
                <div class="yl-minleft-top-ri">
                  <p>DAILY PROFIT</p>
                  <p>16%</p>
                </div>
              </div>
              <div class="yl-minleft-xian"></div>
              <div class="yl-minleft-top yl-gr">
                <div class="yl-minleft-top-le">
                  <p>TOTAL RETURN</p>
                  <p>5,840%</p>
                </div>
                <div class="yl-minleft-top-ri">
                  <p>WITHDRAW TIME</p>
                  <p style="font-weight: 400; font-size: 19px;">ANYTIME</p>
                </div>
              </div>
              <div class="yl-minleft-bot">
                <p>
                  CART WILL BE FULL IN:
                  <span>--:--:--</span>
                </p>
                <p>
                  COMPOUND COUNT:
                  <span>0</span>
                </p>
              </div>
            </div>
            <div class="yl-minleft-f">
              <div class="yl-minleft-f-input">
                <input type="text" v-model="num.number1" />
              </div>
              <p class="yl-minleft-f-text">
                ENTER USDT AMOUNT & CLICK APPROVE BELOW
              </p>
              <button>Approve USDT</button>
            </div>
            <div class="yl-minleft-f">
              <div class="line_holder">
                <p class="item one">
                  <span>Min:</span>
                  10 USDT
                </p>
                <div class="line"></div>
              </div>
              <div class="yl-minleft-f-input">
                <input type="text" v-model="num.number2" />
                <span
                  @click="addJian('+')"
                  class="inputTN__top"
                  style="float: right; margin: 7px 0px 7px 0px;"
                >
                  <svg
                    width="25"
                    height="25"
                    class="icon-plus icon-control"
                    viewBox="0 0 25 25"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <circle
                      cx="12.5"
                      cy="12.5"
                      r="9.375"
                      stroke="#E7FAFF"
                      stroke-width="2"
                    ></circle>
                    <path
                      d="M12.5 15.625L12.5 9.375"
                      stroke="#E7FAFF"
                      stroke-width="2"
                      stroke-linecap="square"
                    ></path>
                    <path
                      d="M15.625 12.5L9.375 12.5"
                      stroke="#E7FAFF"
                      stroke-width="2"
                      stroke-linecap="square"
                    ></path>
                  </svg>
                </span>
                <span
                  @click="addJian('-')"
                  class="inputTN__bottom"
                  style="float: right; margin: 7px 0px 7px 0px;"
                >
                  <svg
                    width="25"
                    height="25"
                    class="icon-minus icon-control"
                    viewBox="0 0 25 25"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <g opacity="0.3">
                      <circle
                        cx="12.5"
                        cy="12.5"
                        r="9.375"
                        stroke="#E7FAFF"
                        stroke-width="2"
                      ></circle>
                      <path
                        d="M15.625 12.5L9.375 12.5"
                        stroke="#E7FAFF"
                        stroke-width="2"
                        stroke-linecap="square"
                      ></path>
                    </g>
                  </svg>
                </span>
              </div>
              <p class="yl-minleft-f-text">
                ENTER USDT AMOUNT & CLICK HIRE BELOW
              </p>
              <button>Hire ? USDT Miners</button>
              <div class="other-button-container">
                <button
                  class="action-enable-btn2"
                  id="withdraw"
                  onclick="sellEggs()"
                  role="button"
                  disabled=""
                  style="display: flex; flex-wrap: wrap;"
                >
                  Sell Miners
                  <br />
                  <div style="display: flex; flex-wrap: wrap;">
                    <span
                      style="font-size: 15px;"
                      class="cooldown"
                      id="cooldown-timer"
                    >
                      in --:--:--
                    </span>
                    <span
                      style="font-size: 15px;"
                      class="tax"
                      id="withdraw-tax"
                    >
                      -80% tax
                    </span>
                  </div>
                </button>

                <button
                  class="action-enable-btn2"
                  id="reinvest"
                  onclick="hatchEggs()"
                  role="button"
                  disabled=""
                  style="display: flex; flex-wrap: wrap;"
                >
                  Compound
                  <span class="compound" style="font-size: 15px;">
                    (
                    <span class="compound" id="compound-bonus">+0% bonus</span>
                    )
                  </span>
                </button>
              </div>
            </div>
          </div>
          <div class="yl-mincont-right">
            <div class="yl-minright-top">
              <div
                v-for="(i, index) in minlist1"
                :key="i"
                class="yl-mintop flex"
              >
                <img src="../assets/图标.png" alt="" />
                <div
                  :class="
                    index == 2 ? 'yl-mintop-text yl-mintext3' : 'yl-mintop-text'
                  "
                >
                  <span>{{ i }}</span>
                  <span v-show="index != 2">?</span>
                </div>
                <div v-show="index == 2" class="yl-minright-text">
                  --:--:--
                </div>
              </div>
            </div>
            <div class="yl-lastline"></div>
            <div class="yl-minright-list">
              <h2>Miner Rules</h2>
              <div></div>
              <div class="yl-minright_lists">
                <div class="yl-list-item">
                  <div>1</div>
                  <p>"Hire Miners" using USDT Tokens</p>
                  <svg
                    width="6"
                    height="73"
                    class="yl-ruleline"
                    viewBox="0 0 6 73"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <rect
                      width="6"
                      height="73"
                      rx="3"
                      fill="white"
                      fill-opacity="0.11"
                    ></rect>
                  </svg>
                </div>
                <div class="yl-list-item">
                  <div>2</div>
                  <p>
                    YOUR MINERS WILL START DIGGING, PLACING THE TOKENS THEY FIND
                    INTO YOUR CART
                  </p>
                  <svg
                    width="6"
                    height="73"
                    class="yl-ruleline"
                    viewBox="0 0 6 73"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <rect
                      width="6"
                      height="73"
                      rx="3"
                      fill="white"
                      fill-opacity="0.11"
                    ></rect>
                  </svg>
                </div>
                <div class="yl-list-item">
                  <div>3</div>
                  <p>
                    YOU CAN COMPOUND YOUR EARNINGS USING THE "COMPOUND" BUTTON
                  </p>
                  <svg
                    width="6"
                    height="73"
                    class="yl-ruleline"
                    viewBox="0 0 6 73"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <rect
                      width="6"
                      height="73"
                      rx="3"
                      fill="white"
                      fill-opacity="0.11"
                    ></rect>
                  </svg>
                </div>
                <div class="yl-list-item">
                  <div>4</div>
                  <p>
                    YOU CAN WITHDRAW THE TOKENS IN YOUR BARREL
                    <br />
                    USING THE "SELL MINERS" BUTTON
                  </p>
                </div>
                <p>Enjoy up to 16% daily rewards and 5,840% ROI</p>
                <hr style="color: #fff;" />
              </div>
            </div>
            <div class="yl-minright-con">
              <p style="text-align: center;">
                2.5% stacking compound bonus every 6 hrs.
                <br />
                <br />
                48 hours cut off time.
                <br />
                <br />
                10 USDT minimum investment.
                <br />
                <br />
                60% feedback for withdrawals that will be
                <br />
                done not after 3 consecutive compounds.(12.5%)
                <br />
                <br />
                Withdrawals will reset daily compound
                <br />
                count back to 0.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Referral Program -->
    <div class="yl-ref">
      <div class="yl-refbox">
        <h1>REFERRAL PROGRAM</h1>
        <p>
          <span>
            Earn 12% of the USDT used to hire miners by anyone who starts mining
            using your link
          </span>
        </p>
        <div class="yl-refcont">
          <div class="yl-refctit">
            <p>
              RERFERRALS:
              <span>(-)</span>
            </p>
            <div class="yl-inputbox flex">
              <p>YOUR LINK:</p>
              <input type="text" class="yl-refinp" placeholder="Referral" />
            </div>
            <div class="yl-refbcon">
              <p>
                <span>You Can Earn USDT Tokens</span>
                For Inviting New Users To Join USDT Machine. The USDT Machine
                contract has a direct, one-level referral system
                <span>that rewards referrer</span>
                when invited users withdraw their tokens. Promote your referral
                link and
                <span>earn 12% referral rewards.</span>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--  How to start mining -->
    <div class="yl-how">
      <div class="yl-howbox">
        <h1>HOW TO START MINING</h1>
        <p>
          <span>HELP AND INSTRUCTIONS FOR DEFI ECO SYSTEM</span>
        </p>
        <div class="yl-howconbox flex">
          <div class="yl-howleft">
            <p>
              COMPLETE
              <span>5</span>
              SIMPLE STEPS
            </p>
            <div class="yl-hownum">
              <div
                class="flex yl-hnumcon"
                v-for="(i, index) in reflist"
                :key="i"
              >
                <div class="yl-hnumber">{{ index + 1 }}</div>
                <div class="yl-hcont">
                  <p>{{ i }}</p>
                </div>
              </div>
            </div>
          </div>
          <div class="yl-howright">
            <div class="yl-hrtit flex">
              <p>INSTRUCTIONS</p>
              <div></div>
            </div>
            <p class="yl-hrcont">
              <span style="color: #48ad92; font-weight: 700;">1.</span>
              Send USDT To Metamask/Trustwallet wallet on Binance smart Chain
              Network (BSC).
            </p>
            <p class="yl-hrcont">
              <span style="color: #48ad92; font-weight: 700;">2.</span>
              In Metamask/Trustwallet Browser Connect to
              <b style="color: #48ad92; font-weight: 700;">PANCAKESWAP</b>
              and swap your tokens to USDT
              <br />
              (USDT BEP20Token)
            </p>
            <p class="yl-hrcont">
              <span style="color: #48ad92; font-weight: 700;">3.</span>
              At usdtmachine.finance site:
              <br />
              <span style="color: #48ad92; font-weight: 700;">A.</span>
              Approve the amount of USDT token you wish to spend.
              <br />
              <span style="color: #48ad92; font-weight: 700;">B.</span>
              Enter the USDT amount to Hire Miners.
              <br />
              <span style="color: #48ad92; font-weight: 700;">C.</span>
              Click Hire miners.
              <br />
              <span style="color: #48ad92; font-weight: 700;">D.</span>
              Compound Daily to hire more miners to increase you'r profit.
              <br />
              <span style="color: #48ad92; font-weight: 700;">E.</span>
              Withdraw Profit using the "Sell Miners" button.
              <br />
            </p>
            <p class="yl-hrcont">
              <span style="color: #48ad92; font-weight: 700;">
                The object of the game
              </span>
              Buying more miners, sooner and more often than other players. This
              in turn earns you more USDT faster. Compounding your daily USDT
              earnings will 3x your miners within 30 days or less.
            </p>
          </div>
        </div>
      </div>
    </div>
    <!-- 尾部 -->
    <div class="yl-footer">
      <div>
        <div class="yl-footer-list">
          <div class="yl-foot-lis">
            <div>
              <svg
                width="32"
                height="33"
                viewBox="0 0 32 33"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M24.5251 8.15336L17.5755 5.17498C16.5693 4.74376 15.4304 4.74376 14.4242 5.17498L7.47461 8.15336C6.98437 8.36346 6.6665 8.84552 6.6665 9.37889V16.3827C6.6665 18.9664 7.91423 21.3909 10.0166 22.8926L14.4499 26.0592C15.3771 26.7215 16.6226 26.7215 17.5498 26.0592L21.9831 22.8926C24.0854 21.3909 25.3332 18.9664 25.3332 16.3827V9.37889C25.3332 8.84552 25.0153 8.36347 24.5251 8.15336ZM20.7807 13.1247C21.1257 12.6934 21.0558 12.0641 20.6245 11.7191C20.1933 11.3741 19.564 11.444 19.219 11.8753L14.5836 17.6695L12.7069 15.7929C12.3164 15.4024 11.6833 15.4024 11.2927 15.7929C10.9022 16.1834 10.9022 16.8166 11.2927 17.2071L13.5644 19.4788C14.1966 20.1109 15.2379 20.0533 15.7964 19.3551L20.7807 13.1247Z"
                  fill="white"
                ></path>
              </svg>
              VERIFIED PUBLIC CONTRACT
            </div>
            <p>
              The USDT Machine contract is public, verified and can be viewed
              here on
              <a>BscScan</a>
              .
            </p>
          </div>
          <div class="yl-foot-lis">
            <div>
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12C22 15.0141 20.6665 17.7167 18.5573 19.5501C18.0996 18.3251 17.306 17.2481 16.2613 16.4465C15.0388 15.5085 13.5409 15 12 15C10.4591 15 8.96118 15.5085 7.73867 16.4465C6.69405 17.2481 5.90038 18.3251 5.44269 19.5501C3.33349 17.7167 2 15.0141 2 12ZM16.8296 20.7059C16.8337 20.7212 16.8381 20.7363 16.8429 20.7512C15.4081 21.5469 13.757 22 12 22C10.243 22 8.59193 21.5469 7.15711 20.7512C7.16185 20.7363 7.16628 20.7212 7.17037 20.7059C7.45525 19.6427 8.08297 18.7033 8.95619 18.0332C9.82942 17.3632 10.8993 17 12 17C13.1007 17 14.1706 17.3632 15.0438 18.0332C15.917 18.7033 16.5448 19.6427 16.8296 20.7059ZM10 9C10 7.89543 10.8954 7 12 7C13.1046 7 14 7.89543 14 9C14 10.1046 13.1046 11 12 11C10.8954 11 10 10.1046 10 9ZM12 5C9.79086 5 8 6.79086 8 9C8 11.2091 9.79086 13 12 13C14.2091 13 16 11.2091 16 9C16 6.79086 14.2091 5 12 5Z"
                  fill="white"
                ></path>
                <rect
                  x="2.5"
                  y="2.5"
                  width="19"
                  height="19"
                  rx="9.5"
                  stroke="white"
                ></rect>
              </svg>
              MINER INFO
            </div>
            <p>
              USDT Machine pays 16% daily, according to the current mining
              efficiency rate. The mining efficiency rate rises and falls as you
              and other players hire miners, compound earnings and Withdraw.
            </p>
          </div>
          <div class="yl-foot-lis">
            <div>
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12C22 15.0141 20.6665 17.7167 18.5573 19.5501C18.0996 18.3251 17.306 17.2481 16.2613 16.4465C15.0388 15.5085 13.5409 15 12 15C10.4591 15 8.96118 15.5085 7.73867 16.4465C6.69405 17.2481 5.90038 18.3251 5.44269 19.5501C3.33349 17.7167 2 15.0141 2 12ZM16.8296 20.7059C16.8337 20.7212 16.8381 20.7363 16.8429 20.7512C15.4081 21.5469 13.757 22 12 22C10.243 22 8.59193 21.5469 7.15711 20.7512C7.16185 20.7363 7.16628 20.7212 7.17037 20.7059C7.45525 19.6427 8.08297 18.7033 8.95619 18.0332C9.82942 17.3632 10.8993 17 12 17C13.1007 17 14.1706 17.3632 15.0438 18.0332C15.917 18.7033 16.5448 19.6427 16.8296 20.7059ZM10 9C10 7.89543 10.8954 7 12 7C13.1046 7 14 7.89543 14 9C14 10.1046 13.1046 11 12 11C10.8954 11 10 10.1046 10 9ZM12 5C9.79086 5 8 6.79086 8 9C8 11.2091 9.79086 13 12 13C14.2091 13 16 11.2091 16 9C16 6.79086 14.2091 5 12 5Z"
                  fill="white"
                ></path>
                <rect
                  x="2.5"
                  y="2.5"
                  width="19"
                  height="19"
                  rx="9.5"
                  stroke="white"
                ></rect>
              </svg>
              SUSTAINABILITY
            </div>
            <p>
              USDT Machine pays a modest 16% daily, allowing investors to rest
              easy knowing that their investments have unlimited growth
              potential and a maximum, improbable risk of less than 16%.
            </p>
          </div>
        </div>
        <div class="yl-footer-new">
          <span style="color: #48ad91;">WARNING:</span>
          USDT Machine is subject to high risk. Please make your investment
          cautiously. Smart Miner and USDT Machine will not be responsible for
          your investment losses. Crypto markets and Blockchain technology are
          high risk! Always do your own due diligence.
        </div>
      </div>
    </div>
    <p>© Copyright USDT Machine . All Rights Reserved</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toplist: ['MINING', 'ERFERRAL', 'HOW TO START', 'ABOUT', 'CONTRACT'],
      showlist: ['Start Miner', 'Contract', 'Telegram', 'Whitepaper', 'Audit'],
      minlist: [
        'TOTAL DEPOSIT COUNT:',
        'CONTRACT BALANCE:',
        'INITIAL DEPOSIT:',
      ],
      minlist1: [
        'Total Deposit:',
        'Sold Miners:',
        ' Time until next compound bonus is activated:',
      ],
      reflist: [
        'ENTER USDT AMOUNT',
        ' CLICK "HIRE MINERS"',
        ' MINERS FIND TOKENS',
        'COMPOUND DAILY',
        'WITHDRAW PROFIT!',
      ],
      num: { number1: 100, number2: 0.01 },
    }
  },
  methods: {
    addJian(a) {
      if (a == '+') {
        this.num.number2 = this.num.number2 + 0.01
      } else {
        if (this.num.number2 <= 0) {
          this.num.number2 = 0
        } else {
          this.num.number2 = this.num.number2 - 0.01
        }
      }
    },
  },
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
svg {
  vertical-align: middle;
}
input,
button {
  outline: none;
  border: 0;
}
a {
  text-decoration: none;
}
ul {
  list-style: none;
}
.flex {
  display: flex;
}
/* 头部 */
.yl-lab {
  position: fixed;
  width: 100%;
  height: 80px;
  background: rgb(32, 32, 32);
  opacity: 0.9;
  z-index: 1000;
  /* line-height: 1.5; */
}
.yl-lab-cont {
  margin: 0 120px;
  padding: 8px 12px;
  padding-right: 50px;
  height: 100%;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
}
.yl-lab-cont img {
  margin-bottom: 10px;
}
.yl-lab-cont ul {
  padding: 15px 0;
  text-align: right;
  list-style-type: none;
  max-height: 10px;
  overflow: hidden;
}

.yl-lab-cont ul li {
  display: inline-flex;
  padding: 0 15px 0 20px;
}
.yl-lab-cont ul li a {
  padding: 0 12px;
  color: white;
  font-weight: 800;
  font-family: 'Poppins-Bold';
  font-size: 16px;
}
.yl-lab-cont .yl-nn {
  height: 40px;
  background: #48b090;
  border-radius: 13px;
  font-weight: 800;
  font-family: 'Poppins-Bold';
  padding: 6px 16px;
  font-size: 20px;
  color: #fff;
  box-sizing: border-box;
  margin-top: 12px;
}
/* 展示 */
.yl-topall {
  width: 100%;
  position: relative;
  height: 700px;
}
.yl-vo {
  position: absolute;
  top: -150px;
  left: 0;
  z-index: -1;
}
.yl-vo video {
  width: 100%;
  height: 100%;
}
.yl-text {
  width: 100%;
  padding: 0 120px;
  box-sizing: border-box;
  border-top: 1px solid rgba(0, 0, 0, 0);
}
.yl-font1 {
  font-family: 'Poppins-Bold';
  font-weight: 700;
  font-size: 38.5px;
  color: rgb(0, 157, 151);
  margin-top: 230px;
  margin-left: -20px;

  width: 46%;
}
.yl-font2 {
  font-size: 18px;
  color: white;
  font-family: 'Poppins-Bold';
  margin-bottom: 32px;
  margin-left: -20px;
  padding: 10px 0;
}
.yl-showlist ul {
  display: flex;
  margin-left: -20px;
}
.yl-showlist ul li {
  background: rgb(72, 167, 143);
  border-radius: 13px;
  font-weight: 800;
  font-family: 'Poppins-Bold';
  padding: 8px 16px;
  font-size: 20px;
  margin-right: 10px;
}
.yl-showlist ul li:nth-child(4) {
  background: rgb(1, 112, 78);
}
.yl-showlist ul li:nth-child(5) {
  background: rgb(1, 112, 78);
}
.yl-biao {
  text-align: center;
  margin-top: 30px;
  position: relative;
  height: 64px;
}
.yl-biao a {
  position: absolute;
  transition: 0.5s linear;
  top: 0;
}
.yl-biao a:hover {
  margin-top: 10px;
  top: -20px;
}
.yl-biao a:hover svg rect {
  fill-opacity: 1;
}
/* MINING */
.yl-min {
  padding: 80px 0;
  background: rgb(58, 57, 58);
}
/* left */
.yl-minbox {
  margin: 0 120px;
}
.yl-minbox h2 {
  font-weight: 800;
  font-size: 50px;
  font-family: 'Poppins-Bold';
  color: #fff;
  margin-bottom: 48px;
}
.yl-mintop {
  margin-bottom: 15px;
  background: rgb(33, 32, 34);
  width: 100%;
  margin-right: 23px;
  font-weight: 400;
  line-height: 1.5;
  border-radius: 14px;
  padding: 10px 0px 10px 10px;
}
.mar .yl-mintop:nth-child(3) {
  margin-right: 0;
}
.yl-mintop img {
  padding: 13px;
  transform: scale(0.8, 0.7);
  margin-right: 5px;
}
.yl-mintop-text {
  font-weight: 700;
  font-size: 24px;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.yl-mincont {
  background: rgb(33, 32, 34);
  border-radius: 8px;
  padding: 30px;
  margin-right: 20px;
}
.yl-mincont-left {
  width: 55%;
  background: rgb(45, 45, 45);
  border-radius: 14px;
  padding: 16px;
}
.yl-minleft-top {
  margin: 10px 0;
  padding: 10px 24px;
  text-align: center;
  box-sizing: border-box;
  line-height: 1.2;
}
.yl-minleft-top img {
  margin-right: 10px;
  vertical-align: middle;
}
.yl-mintop-text1 {
  display: inline-block;
  vertical-align: middle;
  font-size: 2rem !important;
  font-weight: 600;
  color: white;
}
.text {
  text-decoration: underline;
  color: #48b090;
  margin-left: 16px;
}
.yl-mintop-text1 span:nth-child(2) {
  margin-left: 3px;
}
.yl-minleft-t {
  margin: 20px 0 5px 12px;
  align-items: center;
}
.yl-minleft-t h2 {
  font-size: 24px;
  font-family: 'Poppins-Bold';
  font-style: normal;
  font-weight: 600;
  margin: 0;
}
.yl-minleft-t div:nth-child(1) {
  margin-left: 20px;
}
.yl-minp img {
  transform: scale(1, 0.5);
  height: 50%;
  vertical-align: middle;
  padding-right: 10px;
}
.yl-minp {
  vertical-align: middle;
  color: white;
  font-size: 16px;
  font-family: 'Poppins-Bold';
  font-style: normal;
  font-weight: 800;
}
.yl-minp span {
  color: #48b090;
  margin-left: 5px;
}
.yl-marg {
  margin-left: 85px;
}
.yl-minleft-s {
  background: rgb(23, 23, 23);
  padding: 16px;
  border-radius: 13px;
  letter-spacing: -1px;
}
.yl-minleft-top {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
  padding: 0 16px;
  margin-top: 16px;
  color: #fff;
  font-size: 26px;
  font-weight: 800;
}
.yl-minleft-top p + p {
  font-size: 40px;
  line-height: 70px;
}
.yl-minleft-top-le {
  text-align: left;
}
.yl-minleft-top-ri {
  text-align: right;
}
.yl-minleft-xian {
  height: 1px;
  background-color: #303843;
  width: 95%;
  margin: 1rem auto auto;
}
.yl-gr {
  padding: 16px;
  border-radius: 13px;
  background: rgb(72, 172, 147);
  font-size: 23px;
}
.yl-gr p + p {
  font-size: 36px;
  line-height: 70px;
}
.yl-minleft-bot {
  padding: 16px;
  margin-top: 16px;
  border-radius: 13px;
  background: linear-gradient(90.47deg, #4c4c4c -16.53%, #4c4c4c 111.62%),
    #333941 !important;
  color: #fff;
}
.yl-minleft-bot p {
  font-size: 26px;
  font-weight: 800;
  line-height: 38px;
}
.yl-minleft-bot span {
  float: right;
  letter-spacing: 1px;
  font-size: 20px;
  font-weight: 400;
}
.yl-minleft-f {
  padding: 0 16px;
  margin-top: 34px;
}
.yl-minleft-f-input {
  background: hsla(0, 0%, 100%, 0.15);
  border: 2px solid #626f73;
  border-radius: 13px;
  padding: 4.8px 16px;
  outline: none;
  justify-content: space-between;
  align-items: center;
}
.yl-minleft-f-input input {
  width: 50%;
  background-color: transparent;
  font-weight: 800;
  font-size: 26px;
  color: #fff;
}
.yl-minleft-f-text {
  font-style: normal;
  font-weight: 800;
  font-size: 16px;
  letter-spacing: -0.005em;
  text-transform: uppercase;
  color: #fff;
  margin-top: 0.7rem;
  padding-left: 0.5rem;
  margin-bottom: 26px;
}
.yl-minleft-f > button {
  background: rgb(72, 172, 147);
  border-radius: 13px;
  transition: 0.5s linear;
  font-weight: 700;
  font-size: 28px;
  color: #fff;
  outline: none;
  border: none;
  height: 65px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.yl-minleft-f button:hover {
  transform: scale(1.02);
}
.line_holder {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 24px;
  margin-bottom: 16px;
  padding: 8px;
}
.line_holder .item {
  font-weight: 600;
  font-size: 20px;
  color: #fff;
  text-transform: uppercase;
  font-family: 'Poppins-Bold';
  white-space: nowrap;
}
.line_holder .item.one {
  text-align: left;
}
.line_holder .item span {
  font-weight: 400;
  font-family: 'Poppins-Regular';
}
.line_holder .line {
  width: 38%;
  height: 1px;
  background-color: hsla(0, 0%, 100%, 0.1);
}
.icon-control:hover {
  transform: scale(1.1);
}
.other-button-container {
  display: flex;
}
.other-button-container {
  gap: 27px;
}
.action-enable-btn2 {
  border-radius: 13px;
  transition: 0.5s linear;
  opacity: 0.3;
  background: #000;
  font-weight: 700;
  font-size: 28px;
  margin-top: 16px;
  color: #fff;
  outline: none;
  border: none;
  height: 65px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.yl-mincont-right {
  flex: 0 0 auto;

  width: 41.66666667%;
  padding: 0 12px;
  padding-left: 35px;
}
.yl-mincont-right .yl-mintop {
  background: rgb(45, 45, 45);
}
.yl-lastline {
  height: 1px;
  background-color: hsla(0, 0%, 100%, 0.05);
  width: 80%;
  margin: 26px auto;
}
.yl-minright-list > h2 {
  font-style: normal;
  font-weight: 800;
  font-size: 25px;
  letter-spacing: -1px;
  text-transform: uppercase;
  color: #fff;
  margin: 0;
}
.yl-minright-list > h2 + div {
  width: 58px;
  height: 6px;
  background: #fff;
  border-radius: 50px;
}
.yl-minright-text {
  color: #fff;
  font-size: 16px;
  line-height: 40px;
  margin-left: 20px;
}
.yl-mintop .yl-mintext3 {
  font-size: 16px;
  padding-top: 15px;
}

.yl-minright_lists {
  margin-top: 48px;
  display: flex;
  flex-direction: column;
  position: relative;
}
.yl-list-item {
  display: flex;
  align-items: center;
  position: relative;
  margin-bottom: 25px;
}
.yl-list-item > div:first-child {
  background: #2d2d2d;
  border-radius: 50%;
  width: 59px;
  height: 59px;
  color: #fff;
  z-index: 9;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 600;
  font-size: 24px;
  text-transform: uppercase;
  border: 4px solid #39404b;
}
.yl-list-item > div + p {
  font-style: normal;
  font-weight: 500;
  font-size: 17px;
  text-transform: uppercase;
  color: #fff;
  margin-left: 20px;
  width: 422px;
}

.yl-ruleline {
  position: absolute;
  left: 32px;
  bottom: -59px;
  z-index: 1;
}
.yl-list-item + p {
  color: #fff;
  font-size: 15px;
}
hr:not([size]) {
  height: 1px;
}
hr {
  margin: 36px 0;
  background-color: currentColor;
  border: 0;
  opacity: 0.25;
}
.yl-minright-con p {
  font-style: normal;
  font-weight: 500;
  font-size: 17px;
  text-transform: uppercase;
  color: #fff;
}
/*Referral Program  */
.yl-ref {
  padding: 80px 0;
  background: rgb(58, 57, 58);
}
.yl-refbox {
  margin: 0 120px;
  padding: 0 12px;
}
.yl-refbox h1 {
  font-weight: 800;
  font-size: 50px;
  font-family: 'Poppins-Bold';
  color: #fff;
}
.yl-refbox > p {
  margin-bottom: 48px;
  font-weight: 800;
  font-size: 17px;
  color: #48ae91;
}
.yl-refcont {
  background: rgb(40, 40, 40);
  padding: 30px;
  border-radius: 13px;
}
.yl-refctit {
  padding: 16px;
  background: rgb(36, 36, 36);
  border-radius: 13px;
}
.yl-refctit > p {
  font-size: 25px;
  font-weight: 800;
  color: #fff;
  padding-bottom: 5px;
}
.yl-inputbox {
  justify-content: flex-start;
  padding: 16px;
  align-items: center;
  background: #4c4c4c;
  border-radius: 14px;
}
.yl-inputbox > p {
  font-size: 25px;
  font-weight: 800;
  color: #fff;
}
.yl-refinp {
  width: 85%;
  margin-left: 20px;
  border-radius: 13px;
  font-style: normal;
  font-weight: 700;
  color: #fff;
  border: none;
  outline: none;
  font-size: 22px;
  padding: 17.5px;
  box-sizing: border-box;
  transition: 0.2s linear;
  background: rgb(72, 172, 147);
}
.yl-refinp:hover {
  transform: scale(1.01);
}
.yl-refbcon {
  margin: 24px 0;
}
.yl-refbcon > p {
  margin-top: 16px;
  font-size: 20px;
  color: #fff;
  letter-spacing: -0.5px;
  line-height: 30px;
  text-align: center;
}
.yl-refbcon > p > span {
  color: #48ad92;
  font-weight: 700;
}
/*  How to start mining */
.yl-how {
  padding: 80px 0;
  background: rgb(58, 57, 58);
}
.yl-howbox {
  margin: 0 120px;
  padding: 0 12px;
}
.yl-howbox h1 {
  font-weight: 800;
  font-size: 50px;
  font-family: 'Poppins-Bold';
  color: #fff;
}
.yl-howbox > p {
  font-weight: 800;
  font-size: 17px;
  color: #48ae91;
  margin-bottom: 48px;
}
.yl-howconbox {
  padding: 24px;
  background: #212022;
  justify-content: space-between;
  flex-wrap: wrap;
  border-radius: 13px;
}
.yl-howconbox > div:nth-child(1) {
  width: 50%;
}
.yl-howleft {
  background: #2d2d2d;
  border-radius: 14px;
  padding: 16px;
  height: 100%;
}
.yl-howleft > p {
  font-weight: 800;
  font-size: 24px;
  color: white;
}
.yl-howleft > p > span {
  color: #009d97;
}
.yl-hownum {
  margin: 8px;
}
.yl-hnumcon {
  background: rgb(72, 172, 147);
  padding: 8px;
  margin-bottom: 16px;
  border-radius: 13px;
  align-items: center;
}
.yl-hnumber {
  width: 58px;
  height: 58px;
  background: #009d97;
  font-size: 28px;
  color: #ffffff;
  font-weight: 700;
  font-family: 'Poppins-Bold';
  border-radius: 13px;
  align-items: center;
  display: flex;
  justify-content: center;
  margin-right: 15px;
}
.yl-hcont {
  font-weight: 800;
  font-size: 27px;
  color: #fff;
}
.yl-howright {
  width: 42%;
  padding: 0 32px;
}
.yl-hrtit {
  margin-bottom: 16px;
  text-align: left;
  font-weight: 600;
  font-size: 23px;
  color: #fff;
}
.yl-hrtit > div {
  width: 100%;
  margin: 15px 10px 0 10px;
  height: 1px;
  background-color: rgb(55, 56, 57);
}
.yl-hrcont {
  font-size: 18px;
  color: #fff;
  line-height: 30px;
  margin-bottom: 16px;
}
/* 尾部 */
.yl-footer {
  padding: 80px 0;
  background: rgb(58, 57, 58);
}
.yl-footer > div {
  margin: 0 120px;
}
.yl-footer-new {
  border-radius: 13px;
  padding: 24px;
  background: #212022;
  color: #fff;
}
.yl-footer-list {
  display: flex;
}
.yl-foot-lis {
  width: 33%;
  position: relative;
  padding: 24px;
  text-align: center;
}
.yl-foot-lis > div {
  font-weight: 700;
  font-size: 20px;
  color: #fff;
}
.yl-foot-lis p {
  margin-top: 16px;
  font-weight: 500;
  font-size: 16px;
  text-align: center;
  color: #7c7e81;
  letter-spacing: -1px;
}
.yl-foot-lis p a {
  color: #48ad91;
}
.yl-footer + p {
  text-align: center;
  background: rgb(55, 56, 57);
  color: #7c7e81;
  font-weight: 900;
  font-size: 20px;
}
</style>
