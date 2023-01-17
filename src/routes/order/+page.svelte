<script context="module">
	import data from '../../data/order.json';
	export const prerender = true;
</script>

<svelte:head>
		<title>{data.title}</title> 
<meta content='{data.title}' property='og:title'/>
<meta content='{data.title} ' name='twitter:title'/>
<meta content='{data.title}' name='keywords'/>
<meta content='{data.title}' property='og:site_name'/>
<meta content="{data.description}" name="description"/>
<meta content='{data.description}' name='twitter:description'/>
<meta content='summary_large_image' name='twitter:card'/>
<meta content='https://softwaretoko.axcora.com' property='twitter:author'/>
<meta content='https://softwaretoko.axcora.com' name='twitter:site'/>
<meta content='{data.cover}' name='twitter:image'/>
<meta content={data.author} property='og:author'/>
<link rel="canonical" href={data.url} />
<meta content='website' property='og:type'/>
<meta content='index, follow' name='robots'/>
</svelte:head>

<h1><strong><a href={data.url}>{data.title}</a></strong></h1>
  <h2>{data.description}</h2>
	<p>{data.desktop}<br/><a href={data.desktoplink} class="btn btn-outline-dark btn-sm slim mt-1">Order {data.desktoptitle}</a></p>
  <p>{data.cloud}<br/><a href={data.cloudlink} class="btn btn-dark btn-sm slim mt-1">{data.cloudtitle}</a></p>
	<p>{data.app}<br/><a href={data.applink} class="btn btn-outline-dark btn-sm slim mt-1">{data.apptitle}</a>	</p>
  <p>{data.pos}<br/><a href={data.poslink} class="btn btn-dark btn-sm slim mt-1">{data.postitle}</a></p>
