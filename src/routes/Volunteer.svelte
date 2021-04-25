<script>
    // Contributors
	const contributorsDB = (async () => {
		var response = await fetch('https://potion-api.now.sh/table?id=0fb220c98d614169923c9c44240c0327')
		return await response.json()
	})()
</script>

<section>
    <div class="width-restriction">
        <h1>Vounteer with us</h1>
        <br/>
        <h2>People working with us</h2>
        <br/>
        {#await contributorsDB}
				<p>Contributors loading...</p>
			{:then data}
				<div class="row">
					<div class="col-3">
						{#each data as contributor, i}
                        {#if i%3 == 0}
                        <div class="card">
                            <div class="width-restriction">
                                <h3>{contributor.fields.name}</h3>
                                <p>{contributor.fields.role}</p>
                            </div>
                        </div>
						{/if}
                        {/each}
					</div>
                    <div class="col-3">
						{#each data as contributor, i}
                        {#if i%3 == 1}
                        <div class="card">
                            <div class="width-restriction">
                                <h3>{contributor.fields.name}</h3>
                                <p>{contributor.fields.role}</p>
                            </div>
                        </div>
						{/if}
                        {/each}
					</div>
                    <div class="col-3">
						{#each data as contributor, i}
                        {#if i%3 == 2}
                        <div class="card">
                            <div class="width-restriction">
                                <h3>{contributor.fields.name}</h3>
                                <p>{contributor.fields.role}</p>
                            </div>
                        </div>
						{/if}
                        {/each}
					</div>
				</div>
				
			{:catch error}
				<p>There was an error in loading contributors</p>
			{/await}
    </div>
</section>