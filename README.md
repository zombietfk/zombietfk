<style>
.running-across-screen {
  position: absolute;
  top: 50%;
  left: 0;
  transform: translate(-128px, -50%); /* start just off-screen */
  animation: running-across-screen 6s linear infinite;
}

.running-across-screen .bear {
  width: 128px;
  height: 128px;
  background-image: url("./bear_running.png");
  background-repeat: no-repeat;
  background-position: 0 0;
  background-size: 512px 128px;
  animation: bear-sprite-atlas 0.8s steps(4) infinite;
}

@keyframes bear-sprite-atlas {
  from { background-position-x: 0; }
  to   { background-position-x: -512px; }
}

@keyframes running-across-screen {
  from { transform: translate(-128px, -50%); }
  to   { transform: translate(calc(100vw + 128px), -50%); }
}
</style>
