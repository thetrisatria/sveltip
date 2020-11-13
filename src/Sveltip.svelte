<script>
    export let text = "";
    export let light = false;
    export let dark = false;
    export let top = false;
    export let bottom = false;
    export let right = false;
    export let left = false;
  </script>
  
  <div class="container">
    <span class="slot"><slot /></span>
    <div class="bubble" class:light class:dark class:left class:right class:bottom class:top>{text}</div>
  </div>
  
  <style>
    .container {
      position: relative;
      display: block;
    }
    .bubble {
      display: block;
      position: absolute;
      padding: 4px 12px;
      white-space: nowrap;
      border-radius: 4px;
      font-size: .75rem;
      color: inherit;
      -webkit-backdrop-filter: saturate(180%) blur(20px);
      backdrop-filter: saturate(180%) blur(20px);
      box-shadow: 0px 1px 6px rgba(0,0,0,0.2);
      visibility: hidden;
      
    }
    .bubble.light {
      background: rgba(256,256,256,.72)
    }
    .bubble.dark {
      background: rgba(0,0,0,.64);
      color: #fff;
    }
    .bubble.top {
      left: 50%;
      bottom: 100%;
      transform:translateX(-50%);
      margin-bottom: 4px;
    }
    .bubble.bottom {
      left: 50%;
      top: 100%;
      transform:translateX(-50%);
      margin-top: 4px;
    }
    .bubble.right {
      right: 0;
      transform: translateX(100%);
      margin-right: -4px;
    }
    .bubble.left {
      left: 0;
      transform: translateX(-100%);
      margin-left: -4px;
    }
    .slot:hover + .bubble {
      visibility: visible;
      animation: fadein .64s;
    }
    @keyframes fadein {
          from {
              opacity: 0;
          }
          to {
              opacity: 1;
          }
      }
  </style>