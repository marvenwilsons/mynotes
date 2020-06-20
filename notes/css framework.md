---
tags: [Donque CMS]
title: css framework
created: '2020-06-10T01:13:17.261Z'
modified: '2020-06-10T01:14:55.486Z'
---

## css framework

```css
/* app global css */
.fullheight-VH {
    height: 100vh;
  }
  .fullheight-percent {
    height: 100% !important;
  }
  .fh-percent {
    height: 100% !important;
  }
  .footing {
    margin-top: auto;
    bottom: 0;
  }
  
  article,
  aside,
  details,
  figcaption,
  figure,
  footer,
  header,
  hgroup,
  main,
  menu,
  nav,
  section,
  summary {
    box-sizing: border-box;
    display: block;
  }
  /*General Style*/
  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    color: #282828;
  }
  q {
    font-style: italic;
    quotes: "" "";
  }
  img {
    width: 100%;
    height: inherit;
    overflow: hidden;
  }
  /*text colors*/
  
  /*containers*/
  .block {
    display: block;
  }
  .flex {
    display: flex;
  }
  .flexcenter {
    justify-content: center;
    align-content: center;
    align-items: center;
  }
  /*orientation*/
  .flexrow {
    flex-direction: row;
  }
  .flexcol {
    flex-direction: column;
  }
  .spacebetween {
    justify-content: space-between;
  }
  .spacearound {
    justify-content: space-around;
  }
  .flexend {
    justify-content: flex-end;
  }
  .flexstart {
    justify-content: flex-start;
  }
  /*Responsiveness*/
  .flexwrap {
    flex-wrap: wrap;
  }
  
  /*Child*/
  .margincenter {
    margin: auto;
  }
  
  /*positions*/
  .relative {
    position: relative;
  }
  .absolute {
    position: absolute;
  }
  .absolutecenter {
    margin: auto;
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
  }
  /*forms*/
  
  /*spacers*/
  .spacer-w-20 {
    width: 20px;
  }
  .spacer-h-20 {
    height: 20px;
  }
  .spacer-w-40 {
    width: 40px;
  }
  .spacer-h-40 {
    height: 40px;
  }
  /*12 Col Grid System*/
  
  .borderred {
    border: 1px solid red;
  }
  .fullwidth {
    width: 100%;
  }
  /* flex */
  .flex1 {
    flex: 1;
  }
  .flex2 {
    flex: 2;
  }
  .flex3 {
    flex: 3;
  }
  .flex4 {
    flex: 4;
  }
  .flex5 {
    flex: 5;
  }
  .flex6 {
    flex: 6;
  }
  .flex7 {
    flex: 7;
  }
  .flex8 {
    flex: 8;
  }
  .flex9 {
    flex: 9;
  }
  
  .flex10 {
    flex: 10;
  }
  
  /* @others */
  .hide {
    display: none;
  }
  .show {
    display: block;
  }
  
  /* wrappers and containers */
  .contentpad {
    padding: calc(var(--fontSize) * 1.50);
    padding-bottom: calc(var(--fontSize) * 2.25);
    position: relative;
  }
  .block-h1 {
    margin-top: 0px;
    margin-bottom:  calc(var(--fontSize) * 1.50 * 1.50 * 1.50);
    line-height:  calc(var(--fontSize) * 1.50 * 2.10);
    height: calc(var(--fontSize) * 1.50 * 1.90);
    font-size: calc(var(--fontSize) * 1.25 * 1.25 * 1.25 * 1.25 * 1.25 * 1.25);
    color: rgba(51, 51, 51, 0.774);
  }
  .block-h6 {
    margin-top: 0px;
    margin-bottom:  calc(var(--fontSize) * 1.50 * 1.00);
    line-height:  calc(var(--fontSize) * 1.50 * 2.10);
    height: calc(var(--fontSize) * 1.50 * 1.90);
    font-size: calc(var(--fontSize) * 1.25);
    color: rgba(51, 51, 51, 0.774);
  }
  .block-p {
    margin: 0px;
    padding: 0px;
    line-height:  calc(var(--fontSize) * 1.65);
  }
  /* heights */
  .h-1s{
    height: calc(var(--fontSize) * 1.50 * 1.50 * 1.50 * 1.33);
  }
  .h-2s{
    height: calc(var(--fontSize) * 1.50 * 1.50 * 1.50 * 1.50 * 1.50 * 1.18);
  }
  /* @paddings */
  .pad050 {
    padding: calc(var(--fontSize) * 0.5);
  }
  .pad025 {
    padding: calc(var(--fontSize) * 0.25);
  }
  .pad125 {
    padding: calc(var(--fontSize) * 1.25);
  }
  .pad1ln {
    padding: calc(var(--fontSize) * 1.50);
  }
  /* shadow */
  .nodeShadow{
    -webkit-box-shadow: 0px 0px 13px -5px rgba(0,0,0,0.75);
    -moz-box-shadow: 0px 0px 13px -5px rgba(0,0,0,0.75);
    box-shadow: 0px 0px 13px -5px rgba(0,0,0,0.75);
  }
  /* padding left, padding right */
  .padleft025 {
    padding-left: calc(var(--fontSize) * 0.25);
  }
  .padleft050 {
    padding-left: calc(var(--fontSize) * 0.5);
  }
  .padright025 {
    padding-right: calc(var(--fontSize) * 0.25);
  }
  .padright050 {
    padding-right: calc(var(--fontSize) * 0.5);
  }
  .padleft125 {
    padding-left: calc(var(--fontSize) * 1.25);
  }
  .padright125 {
    padding-right: calc(var(--fontSize) * 1.25);
  }
  .padleft-1ln {
    padding-left: calc(var(--fontSize) * 1.50);
  }
  .padright-1ln {
    padding-right: calc(var(--fontSize) * 1.50);
  }
  
  /* padding top */
  .padtop-1ln {
    padding-top: calc(var(--fontSize) * 1.50);
  }
  .padtop125 {
    padding-top: calc(var(--fontSize) * 1.25);
  }
  .padtop025 {
    padding-top: calc(var(--fontSize) * 0.25);
  }
  .padtop050 {
    padding-top: calc(var(--fontSize) * 0.5);
  }
  
  /* padding bottom */
  .padbottom125 {
    padding-bottom: calc(var(--fontSize) * 1.25);
  }
  .padbottom025 {
    padding-bottom: calc(var(--fontSize) * 0.25);
  }
  .padbottom050 {
    padding-bottom: calc(var(--fontSize) * 0.5);
  }
  .padbottom-1ln {
    padding-bottom: calc(var(--fontSize) * 1.50);
  }
  .padtop-1ln {
    padding-top: calc(var(--fontSize) * 1.50);
  }
  
  /* margin top */
  .margintop025 {
    margin-top: calc(var(--fontSize) * 0.25);
  }
  .margintop125 {
    margin-top: calc(var(--fontSize) * 1.25);
  }
  .margintop050 {
    margin-top: calc(var(--fontSize) * 0.5);
  }
  .margintop1ln {
    margin-top: calc(var(--fontSize) * 1.50);
  }
  .margintop1s {
    margin-top:  calc(var(--fontSize) * 1.50 * 1.50 * 1.50) !important;
  }
  
  .margin050 {
    margin: calc(var(--fontSize) * 0.5);
  }
  .margin025 {
    margin: calc(var(--fontSize) * 0.25);
  }
  .margin125 {
    margin: calc(var(--fontSize) * 1.25);
  }
  
  
  .marginright025 {
    margin-right: calc(var(--fontSize) * 0.25);
  }
  .marginright125 {
    margin-right: calc(var(--fontSize) * 1.25);
  }
  .marginright050 {
    margin-right: calc(var(--fontSize) * 0.50);
  }
  
  
  .marginbottom025{
    margin-bottom: calc(var(--fontSize) * 0.25);
  }
  .marginbottom050{
    margin-bottom: calc(var(--fontSize) * 0.50);
  }
  .marginbottom125{
    margin-bottom: calc(var(--fontSize) * 1.25);
  }
  .marginbottom1ln {
    margin-bottom: calc(var(--fontSize) * 1.50);
  }
  .marginbottom1s {
    margin-bottom:  calc(var(--fontSize) * 1.50 * 1.50 * 1.50) !important;
  }
  
  .marginleft025 {
    margin-left: calc(var(--fontSize) * 0.25);
  }
  .marginleft050 {
    margin-left: calc(var(--fontSize) * 0.50);
  }
  .marginleft125 {
    margin-left: calc(var(--fontSize) * 1.25);
  }
  
  .overflowhidden {
    overflow: hidden !important;
  }
  .aut {
    overflow: auto !important;
  }
  
  /* button reset */
  .buttonreset {
    display: inline-block;
    border: none;
    text-decoration: none;
    cursor: pointer;
    text-align: center;
    transition: background 250ms ease-in-out, transform 150ms ease;
    -webkit-appearance: none;
    -moz-appearance: none;
    outline: none;
  }
  .dq-button {
    display: inline-block;
    border: none;
    margin: 0;
    text-decoration: none;
    cursor: pointer;
    text-align: center;
    transition: background 250ms ease-in-out, transform 150ms ease;
    -webkit-appearance: none;
    -moz-appearance: none;
    padding: calc(var(--fontSize) * 0.5);
    outline: none;
  }
  .dqbtnbg {
    color: #727272;
  }
  .dqbtnbg:hover {
    transition: 0.3s;
    color: rgba(0, 0, 0, 0.89);
  }
  .btnblue {
    background:rgba(66, 134, 244, 0.815);
    color:white;
    border-radius: 50px;
    outline: none;
  }
  .btnblue:hover {
    background:rgb(66, 134, 244);
  }
  .btntr {
    background:none;
    border: 1px solid lightgray;
    border-radius: 50px;
    font-weight: 700;
    color: rgb(68, 68, 68);
    outline: none;
  }
  .btntr:hover {
    background: rgba(211, 211, 211, 0.267);
    outline: none;
  }
  
  
  .canceldef {
    border-style: none;
    outline: none;
  }
  
  .pointer {
    cursor: pointer;
  }
  .notallowed {
    cursor:  not-allowed;
  }
  .colorinherit {
    color: inherit;
  }
  
  .err {
    color: var(--err);
  }
  .bordererr {
    border: 1px solid #ae11002c;
  }
  .backgrounderr {
    background: #ae11001a;
    color: rgb(107, 4, 4);
    border-left: 5px solid  #ae110059;
    border-top: 1px solid #ae110059;
    border-right: 1px solid #ae110059;
    border-bottom: 1px solid #ae110059;
  }
  
  .backgroundsuc{
    background: #dff0d8;
    color: #417946;
    border-left: 5px solid #41794683;
    border-top: 1px solid #41794683;
    border-bottom: 1px solid #41794683;
    border-right: 1px solid #41794683;
  }
  .backgroundinfo{
    background:#629af47e;
    color:#206add;
    border-left: 5px solid #629af4;
    border-top: 1px solid #629af4;
    border-bottom: 1px solid #629af4;
    border-right: 1px solid #629af4;
  }
  .backgroundwarn{
    background: rgba(255, 166, 0, 0.253);
    color:rgb(90, 62, 11);
    border-left: 5px solid orange;
    border-top: 1px solid orange;
    border-bottom: 1px solid orange;
    border-right: 1px solid orange;
  }
  
  
  /* My Own Style ( dq framework 1.2 )
       ============================================================================*/
  :root {
    --fontSize: 16px;
    --ln: 1.5rem;
  }
  html {
    font-size: var(--fontSize);
  }
  body {
    line-height: var(--ln);
  }
  .container.text {
    max-width: 40rem;
  }
  p,
  blockquote,
  ul,
  ol,
  dl {
    margin: 0 0 var(--ln) 0;
  }
  hr {
    margin: 1.5rem 0 1.5rem 0;
  }
  
  h1 {
    font-size: calc(var(--fontSize) * 1.25 * 1.25 * 1.25 * 1.25 * 1.25 * 1.25);
  }
  h2 {
    font-size: calc(var(--fontSize) * 1.25 * 1.25 * 1.25 * 1.25 * 1.25);
  }
  h3 {
    font-size: calc(var(--fontSize) * 1.25 * 1.25 * 1.25 * 1.25);
  }
  h4 {
    font-size: calc(var(--fontSize) * 1.25 * 1.25 * 1.25);
  }
  h5 {
    font-size: calc(var(--fontSize) * 1.25 * 1.25);
  }
  h6 {
    font-size: calc(var(--fontSize) * 1.25);
  }
  
  h1 {
    line-height: calc(var(--ln) * 2.65);
    margin-top: calc(var(--ln) * 2);
    margin-bottom: calc(var(--ln) * 1.35);
  }
  h2 {
    line-height: calc(var(--ln) * 2.65);
    margin-top: calc(var(--ln) * 1.35);
    margin-bottom: var(--ln);
  }
  h3 {
    line-height: calc(var(--ln) * 1.65);
    margin-top: calc(var(--ln) * 1.35);
    margin-bottom: var(--ln);
  }
  h4 {
    line-height: var(--ln) * 1.65;
    margin-top: calc(var(--ln) * 1.35);
    margin-bottom: var(--ln);
  }
  h5 {
    line-height: var(--ln);
    margin-top: calc(var(--ln) * 1.15);
    margin-bottom: calc(var(--ln) * 0.85);
  }
  h6 {
    line-height: var(--ln);
    margin-top: calc(var(--ln) * 1.15);
    margin-bottom: calc(var(--ln) * 0.85);
  }
  
  
  /* dq input normalize */
  .dqinp {
    border: 1px solid #a9a9a9;
    color: rgba(0, 0, 0, 0.89);
  }
  .dqinp:active {
    outline: none;
  }
  .dqinp:focus {
    outline: none;
  }
  .dqinplabel {
    color:rgba(0, 0, 0, 0.89);
  }
  
  .borderRad4{
    border-radius: 4px;
    overflow:hidden;
  }
  
  body {
    /* background: linear-gradient(to bottom, #ffffff, #ffffff 95%, #bda1a164 100%, #aaaaaa34); */
    background-size: 100% var(--ln);
  }
  
  #spreketek{
    background: linear-gradient(to bottom, #ffffff, #ffffff 95%, #bda1a164 100%, #aaaaaa34);
    background-size: 100% var(--ln);
  }
  
  ._global {
    width: 800px;
  }
  
```
