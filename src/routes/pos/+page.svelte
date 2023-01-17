<script context="module">
	import data from '../../data/poseo.json';
	import datas from '../../data/pos.json';
	export const prerender = true;
</script>
<svelte:head>
		<title>{data.title}</title> 
<meta content={data.title} property='og:title'/>
<meta content={data.title} name='twitter:title'/>
<meta content={data.title} name='keywords'/>
<meta content={data.title} property='og:site_name'/>
<meta content={data.description} name="description"/>
<meta content={data.description} name='twitter:description'/>
<meta content='summary_large_image' name='twitter:card'/>
<meta content='https://softwaretoko.axcora.com' property='twitter:author'/>
<meta content='https://softwaretoko.axcora.com' name='twitter:site'/>
<meta content={data.cover} name='twitter:image'/>
<meta content={data.author} property='og:author'/>
<link rel="canonical" href={data.url} />
<meta content='website' property='og:type'/>
<meta content='index, follow' name='robots'/>
</svelte:head>

<h1><strong><a href={data.url}>{data.title}</a></strong></h1>
<p>{data.info}</p>
<div class="ratio ratio-16x9">
<iframe src="https://www.youtube.com/embed/{data.video}" class="rounded shadow" title="{data.description}" allowfullscreen></iframe>
</div>
<h2 class="mt-3">{data.description}</h2>
  <div class="row">
  {#each datas as item}
<a href={item.link} class="col-md-12 p-3">
<img alt={item.description} loading="lazy" width="100%" height="100%" class="img-fluid rounded" src={item.image}/>
<h3>{item.title}</h3>
<p>{item.description}</p>
</a>
{/each}
</div>