<script>
  export let env;
</script>

<head>
  <meta charset="utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <title>Completed - NewsFlash | Home</title>
  <base href={env.baseurl}>
  <!-- Favicon -->
  <link
    rel="icon"
    type="image/png"
    sizes="32x32"
    href="media/images/favicon.png"
  />
  <!-- Remix icons -->
  <link
    href="https://cdn.jsdelivr.net/npm/remixicon@2.5.0/fonts/remixicon.css"
    rel="stylesheet"
  />
  <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
  <!-- Swiper.js styles -->
  <link rel="stylesheet" href="css/swiper-bundle.min.css" />
  <!-- Custom styles -->
  <link rel="stylesheet" href="global.css" />

  <!-- Swiper.js -->
  <script type="module" src="https://cdn.jsdelivr.net/gh/livebloggerofficial/News-Ticker@main/main.js"></script>
  <!-- Swiper.js -->
  <script type="module" src="js/script.js"></script>
  <script type="module" src="js/swiper-bundle.min.js"></script>
  <!-- Custom script -->
  <!-- Custom script -->
  <script type="module" src="js/main.js"></script>
  <script type="module" src={`${env.entrypointJS}/core/main.js`}></script>

  <link rel="icon" type="image/svg+xml" href="media/logo.svg" />
  <link rel="stylesheet" href={`${env.entrypointJS}/bundle.css`} />
</head>
