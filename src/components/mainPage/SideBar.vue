<template>
  <div class="sidebar-container">
    <div class="sidebar-list-card">
      <div class="sidebar-list-item" @click="gotomain">
        <div class="sidebar-list-item-img-box">
          <img src="@/assets/icon/融合频道.png" />
        </div>
        <div class="sidebar-list-item-intro">首页</div>
      </div>
      <div class="sidebar-list-item" @click="gotoActive">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scopeyt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scopeyt-icon">
              <path
                d="M10,18v-6l5,3L10,18z M17,3H7v1h10V3z M20,6H4v1h16V6z M22,9H2v12h20V9z M3,10h18v10H3V10z"
                class="style-scopeyt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">订阅内容</div>
      </div>
    </div>

    <div class="sidebar-list-card">
      <div class="sidebar-list-item" @click="gotoPlayList(watch)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M14.97,16.95L10,13.87V7h2v5.76l4.03,2.49L14.97,16.95z M22,12c0,5.51-4.49,10-10,10S2,17.51,2,12h1c0,4.96,4.04,9,9,9 s9-4.04,9-9s-4.04-9-9-9C8.81,3,5.92,4.64,4.28,7.38C4.17,7.56,4.06,7.75,3.97,7.94C3.96,7.96,3.95,7.98,3.94,8H8v1H1.96V3h1v4.74 C3,7.65,3.03,7.57,3.07,7.49C3.18,7.27,3.3,7.07,3.42,6.86C5.22,3.86,8.51,2,12,2C17.51,2,22,6.49,22,12z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">观看记录</div>
      </div>
      <div class="sidebar-list-item" @click="goto">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M10,8l6,4l-6,4V8L10,8z M21,3v18H3V3H21z M20,4H4v16h16V4z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">我的影片</div>
      </div>
      <div class="sidebar-list-item" @click="gotoPlayList(collect)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M14.97,16.95L10,13.87V7h2v5.76l4.03,2.49L14.97,16.95z M12,3c-4.96,0-9,4.04-9,9s4.04,9,9,9s9-4.04,9-9S16.96,3,12,3 M12,2c5.52,0,10,4.48,10,10s-4.48,10-10,10S2,17.52,2,12S6.48,2,12,2L12,2z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">我的收藏</div>
      </div>
      <div class="sidebar-list-item" @click="gotoPlayList(like)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M18.77,11h-4.23l1.52-4.94C16.38,5.03,15.54,4,14.38,4c-0.58,0-1.14,0.24-1.52,0.65L7,11H3v10h4h1h9.43 c1.06,0,1.98-0.67,2.19-1.61l1.34-6C21.23,12.15,20.18,11,18.77,11z M7,20H4v-8h3V20z M19.98,13.17l-1.34,6 C18.54,19.65,18.03,20,17.43,20H8v-8.61l5.6-6.06C13.79,5.12,14.08,5,14.38,5c0.26,0,0.5,0.11,0.63,0.3 c0.07,0.1,0.15,0.26,0.09,0.47l-1.52,4.94L13.18,12h1.35h4.23c0.41,0,0.8,0.17,1.03,0.46C19.92,12.61,20.05,12.86,19.98,13.17z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">喜欢的影片</div>
      </div>
    </div>

    <div class="sidebar-list-card">
      <label>探索发现</label>
      <div class="sidebar-list-item" @click="gotoarea(life)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M14.72,17.84c-0.32,0.27-0.83,0.53-1.23,0.66c-1.34,0.33-2.41-0.34-2.62-0.46c-0.21-0.11-0.78-0.38-0.78-0.38 s0.35-0.11,0.41-0.13c1.34-0.54,1.89-1.24,2.09-2.11c0.2-0.84-0.16-1.56-0.31-2.39c-0.12-0.69-0.11-1.28,0.12-1.9 c0.02-0.05,0.12-0.43,0.12-0.43s0.11,0.35,0.13,0.41c0.71,1.51,2.72,2.18,3.07,3.84c0.03,0.15,0.05,0.3,0.05,0.46 C15.8,16.3,15.4,17.26,14.72,17.84z M12.4,4.34c-0.12,0.08-0.22,0.15-0.31,0.22c-2.99,2.31-2.91,5.93-2.31,8.55l0.01,0.03l0.01,0.03 c0.06,0.35-0.05,0.7-0.28,0.96c-0.24,0.26-0.58,0.41-0.95,0.41c-0.44,0-0.85-0.2-1.22-0.6c-0.67-0.73-1.17-1.57-1.5-2.46 c-0.36,0.77-0.75,1.98-0.67,3.19c0.04,0.51,0.12,1,0.25,1.43c0.18,0.6,0.43,1.16,0.75,1.65c1.05,1.66,2.88,2.82,4.78,3.05 c0.42,0.05,0.85,0.08,1.26,0.08c1.34,0,3.25-0.27,4.74-1.57c1.77-1.56,2.35-3.99,1.44-6.06c-0.04-0.1-0.06-0.14-0.09-0.19 l-0.04-0.08c-0.21-0.42-0.47-0.81-0.75-1.14c-0.24-0.3-0.48-0.56-0.79-0.83c-0.3-0.27-0.64-0.51-1-0.77 c-0.46-0.33-0.93-0.67-1.38-1.09C12.98,7.83,12.3,6.11,12.4,4.34 M14.41,2c0,0-0.2,0.2-0.56,0.99c-0.66,1.92-0.15,3.95,1.34,5.39 c0.73,0.69,1.61,1.17,2.36,1.84c0.32,0.29,0.62,0.59,0.89,0.93c0.36,0.42,0.66,0.89,0.91,1.38c0.05,0.1,0.1,0.2,0.14,0.3 c1.12,2.55,0.36,5.47-1.73,7.31C16.23,21.47,14.22,22,12.22,22c-0.47,0-0.95-0.03-1.41-0.09c-2.29-0.28-4.42-1.66-5.63-3.57 c-0.39-0.6-0.68-1.26-0.88-1.93c-0.16-0.54-0.25-1.1-0.29-1.67c-0.12-1.88,0.67-3.63,1.08-4.31c0.41-0.69,1.55-2.18,1.55-2.18 s0,0.03-0.01,0.09C6.41,10.11,7,11.88,8.22,13.22c0.15,0.17,0.27,0.22,0.34,0.22c0.06,0,0.09-0.04,0.08-0.09 C7.79,9.59,8.37,6,11.35,3.7c0.59-0.46,1.51-0.94,1.98-1.18C13.8,2.28,14.41,2,14.41,2L14.41,2z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">生活</div>
      </div>
      <div class="sidebar-list-item" @click="gotoarea(music)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M12,4v9.38C11.27,12.54,10.2,12,9,12c-2.21,0-4,1.79-4,4c0,2.21,1.79,4,4,4s4-1.79,4-4V8h6V4H12z M9,19c-1.66,0-3-1.34-3-3 s1.34-3,3-3s3,1.34,3,3S10.66,19,9,19z M18,7h-5V5h5V7z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">音乐</div>
      </div>
      <div class="sidebar-list-item" @click="gotoarea(animation)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M22.01,4.91l-0.5-2.96L1.64,5.19L2,8v13h20V8H3.06L22.01,4.91z M5,9l1,3h3L8,9h2l1,3h3l-1-3h2l1,3h3l-1-3h3v11H3V9H5z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">番剧</div>
      </div>
      <div class="sidebar-list-item" @click="gotoarea(game)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M10,12H8v2H6v-2H4v-2h2V8h2v2h2V12z M17,12.5c0-0.83-0.67-1.5-1.5-1.5S14,11.67,14,12.5c0,0.83,0.67,1.5,1.5,1.5 S17,13.33,17,12.5z M20,9.5C20,8.67,19.33,8,18.5,8S17,8.67,17,9.5c0,0.83,0.67,1.5,1.5,1.5S20,10.33,20,9.5z M16.97,5.15l-4.5,2.53 l-0.49,0.27l-0.49-0.27l-4.5-2.53L3,7.39v6.43l8.98,5.04l8.98-5.04V7.39L16.97,5.15 M16.97,4l4.99,2.8v7.6L11.98,20L2,14.4V6.8 L6.99,4l4.99,2.8L16.97,4L16.97,4z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">游戏</div>
      </div>
      <div class="sidebar-list-item" @click="gotoarea(tech)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M17 3V5V6V10V10.51L16.99 10.97C16.94 13.1 15.66 14.94 13.74 15.67H13.72L13.66 15.69L13 15.95V16.65V19V20H14V21H15H10V20H11V19V16.65V15.95L10.34 15.71L10.26 15.68H10.25C8.33 14.95 7.05 13.11 7 10.98V10.51V10V6V5V3H17ZM18 2H6V5H4V6V10V11H6.01C6.07 13.53 7.63 15.78 9.97 16.64C9.98 16.64 9.99 16.64 10 16.65V19H9V20H8V22H16V20H15V19H14V16.65C14.01 16.65 14.02 16.65 14.03 16.64C16.36 15.78 17.93 13.54 17.99 11H20V10V6V5H18V2ZM18 10V6H19V10H18ZM5 10V6H6V10H5Z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">科技</div>
      </div>
      <div class="sidebar-list-item" @click="gotoarea(fashion)">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M12.5,6.44v-0.5C13.36,5.71,14,4.93,14,4c0-1.1-0.9-2-2-2s-2,0.9-2,2h1c0-0.55,0.45-1,1-1s1,0.45,1,1s-0.45,1-1,1h-0.5v1.44 L4,13h2v6h1v2h1v-2h2v3h1v-3h2v2h1v-2h1v-3h3v-3h2L12.5,6.44z M6.66,12L12,7.33L17.34,12H6.66z M14,18H7v-5h7V18z M15,15v-2h2v2H15z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">时尚</div>
      </div>
    </div>

    <div class="sidebar-list-card">
      <!-- <div class="sidebar-list-item" @click="goto">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M12,9c1.65,0,3,1.35,3,3s-1.35,3-3,3s-3-1.35-3-3S10.35,9,12,9 M12,8c-2.21,0-4,1.79-4,4s1.79,4,4,4s4-1.79,4-4 S14.21,8,12,8L12,8z M13.22,3l0.55,2.2l0.13,0.51l0.5,0.18c0.61,0.23,1.19,0.56,1.72,0.98l0.4,0.32l0.5-0.14l2.17-0.62l1.22,2.11 l-1.63,1.59l-0.37,0.36l0.08,0.51c0.05,0.32,0.08,0.64,0.08,0.98s-0.03,0.66-0.08,0.98l-0.08,0.51l0.37,0.36l1.63,1.59l-1.22,2.11 l-2.17-0.62l-0.5-0.14l-0.4,0.32c-0.53,0.43-1.11,0.76-1.72,0.98l-0.5,0.18l-0.13,0.51L13.22,21h-2.44l-0.55-2.2l-0.13-0.51 l-0.5-0.18C9,17.88,8.42,17.55,7.88,17.12l-0.4-0.32l-0.5,0.14l-2.17,0.62L3.6,15.44l1.63-1.59l0.37-0.36l-0.08-0.51 C5.47,12.66,5.44,12.33,5.44,12s0.03-0.66,0.08-0.98l0.08-0.51l-0.37-0.36L3.6,8.56l1.22-2.11l2.17,0.62l0.5,0.14l0.4-0.32 C8.42,6.45,9,6.12,9.61,5.9l0.5-0.18l0.13-0.51L10.78,3H13.22 M14,2h-4L9.26,4.96c-0.73,0.27-1.4,0.66-2,1.14L4.34,5.27l-2,3.46 l2.19,2.13C4.47,11.23,4.44,11.61,4.44,12s0.03,0.77,0.09,1.14l-2.19,2.13l2,3.46l2.92-0.83c0.6,0.48,1.27,0.87,2,1.14L10,22h4 l0.74-2.96c0.73-0.27,1.4-0.66,2-1.14l2.92,0.83l2-3.46l-2.19-2.13c0.06-0.37,0.09-0.75,0.09-1.14s-0.03-0.77-0.09-1.14l2.19-2.13 l-2-3.46L16.74,6.1c-0.6-0.48-1.27-0.87-2-1.14L14,2L14,2z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">设定</div>
      </div> -->
      <div class="sidebar-list-item" @click="gotore">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M13.18,4l0.24,1.2L13.58,6h0.82H19v7h-5.18l-0.24-1.2L13.42,11H12.6H6V4H13.18 M14,3H5v18h1v-9h6.6l0.4,2h7V5h-5.6L14,3 L14,3z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">检举记录</div>
      </div>
      <!-- <div class="sidebar-list-item" @click="goto">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M15.36,9.96c0,1.09-0.67,1.67-1.31,2.24c-0.53,0.47-1.03,0.9-1.16,1.6L12.85,14h-1.75l0.03-0.28 c0.14-1.17,0.8-1.76,1.47-2.27c0.52-0.4,1.01-0.77,1.01-1.49c0-0.51-0.23-0.97-0.63-1.29c-0.4-0.31-0.92-0.42-1.42-0.29 c-0.59,0.15-1.05,0.67-1.19,1.34L10.32,10H8.57l0.06-0.42c0.2-1.4,1.15-2.53,2.42-2.87c1.05-0.29,2.14-0.08,2.98,0.57 C14.88,7.92,15.36,8.9,15.36,9.96z M12,18c0.55,0,1-0.45,1-1s-0.45-1-1-1s-1,0.45-1,1S11.45,18,12,18z M12,3c-4.96,0-9,4.04-9,9 s4.04,9,9,9s9-4.04,9-9S16.96,3,12,3 M12,2c5.52,0,10,4.48,10,10s-4.48,10-10,10S2,17.52,2,12S6.48,2,12,2L12,2z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">说明</div>
      </div>
      <div class="sidebar-list-item" @click="goto">
        <div class="sidebar-list-item-img-box">
          <svg
            viewBox="0 0 24 24"
            preserveAspectRatio="xMidYMid meet"
            focusable="false"
            class="style-scope yt-icon"
            style="
              pointer-events: none;
              display: block;
              width: 100%;
              height: 100%;
            "
            fill="white"
          >
            <g class="style-scope yt-icon">
              <path
                d="M13,14h-2v-2h2V14z M13,5h-2v6h2V5z M19,3H5v16.59l3.29-3.29L8.59,16H9h10V3 M20,2v15H9l-5,5V2H20L20,2z"
                class="style-scope yt-icon"
              ></path>
            </g>
          </svg>
        </div>
        <div class="sidebar-list-item-intro">提供意见</div>
      </div> -->
    </div>
  </div>
</template>

<script setup lang="ts">
import { useRouter } from "vue-router";
import { useUserStore } from "@/stores/user";
import { ElMessage } from "element-plus";
const store = useUserStore();
const watch = "watch";
const like = "like";
const collect = "collect";
const music = "music";
const animation = "animation";
const game = "game";
const tech = "tech";
const life = "life";
const fashion = "fashion";
const router = useRouter();
async function gotoPlayList(query) {
  if (store.isLoggedIn) {
    await router.push({
      path: `/playlist`,
      query: {
        query,
      },
    });
    location.reload();
  } else {
    ElMessage({
      message: "请先登录",
      type: "warning",
    });
  }
}
const gotomain = () => {
  router.push({
    path: `/main`,
  });
};
const gotoarea = (query) => {
  router.push({
    path: `/v/${query}`,
    query: {
      query,
    },
  });
};
const gotore = () => {
  router.push({
    path: `/report`,
  });
};
async function goto() {
  if (store.isLoggedIn) {
    await router.push({
      path: `/user/${store.id}/main`,
    });
    location.reload();
  } else {
    ElMessage({
      message: "请先登录",
      type: "warning",
    });
  }
}
const gotoActive = (path) => {
  if (store.isLoggedIn) {
    router.push("/active");
  } else {
    ElMessage({
      message: "请先登录",
      type: "warning",
    });
  }
};
</script>

<style lang="scss" scoped>
.sidebar-container {
  position: fixed;
  overflow-x: hidden;
  width: 240px;
  background: #0f0f0f;
  height: calc(100vh - 3.280609vw);
  z-index: 99;
  overflow-y: auto;
  &::-webkit-scrollbar {
    width: 0;
  }
  &:hover::-webkit-scrollbar {
    width: 0.585823vw;
  }

  .sidebar-list-card {
    border-bottom: 0.058582vw solid rgb(75, 75, 75);
    padding: 0.702988vw;
    width: calc((14.059754vw) - 0.585823vw);
    background-color: #0f0f0f;
    margin-bottom: 10px;
    label {
      padding-left: 12px;
      display: block;
      margin-bottom: 10px;
    }
    .sidebar-list-item {
      display: flex;
      align-items: center;
      width: 100%;
      height: 2.443292vw;
      background-color: #0f0f0f;
      margin-bottom: 5px;
      padding: 0.702988vw;
      border-radius: 0.615823vw;
      cursor: pointer;
      &:hover {
        background-color: #363636;
      }
      .sidebar-list-item-img-box {
        width: 1.405975vw;
        height: 1.405975vw;
        margin-right: 1.405975vw;
        img {
          width: 100%;
          height: 100%;
        }
      }
      .sidebar-list-item-intro {
        font-size: 0.877914vw;
      }
    }
  }
}
</style>
