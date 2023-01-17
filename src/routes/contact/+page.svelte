<script context="module">
	import data from '../../data/contact.json';
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
  <h2>{data.description}</h2>
<form action="https://airform.io/axcora@gmail.com" method="post">
  <input class="form-control p-1 mt-1 mb-1" type="text" name="name" placeholder="Whatsapp & Nama">
  <textarea class="form-control p-1 mt-1 mb-1" name="message" placeholder="Masukan Pesan"></textarea>
  <button class="btn btn-dark mt-1 ">Kirim pesan</button>
</form>

<p class="mt-3"><strong>{data.company}</strong></p>
<p>{data.address}</p>
<p>{data.wa}</p>
<p>{data.call}</p>