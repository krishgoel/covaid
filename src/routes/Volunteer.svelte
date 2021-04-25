<script>
    // Contributors
	const contributorsDB = (async () => {
		var response = await fetch('https://potion-api.now.sh/table?id=0fb220c98d614169923c9c44240c0327')
		return await response.json()
	})()
</script>

<section>
    <div class="width-restriction" style="width: 70%">
        <h1>Vounteer with us</h1>
        <br/>
        <p>
            CovAID is the joint initiative of 5 Sanskriti School students. We have initiated a unified online platform for smooth and accurate dispersal of information regarding availability of Covid-19 resources in the National Capital Region. We will be posting verified updates on the platform - checking the updated availability by calling hospitals and drug sellers at fixed intervals. 
            <br/><br/>
            For our initiative to maximise its reach and resourcefulness, <strong>we need a bigger working force, which can regularly update the data</strong>. They will be allotted time slots of upto 2 hours, in which they have to call the assigned hospitals and suppliers. <strong>All volunteers will be acknowledged via verifiable certificates</strong>.
            <br/><br/>
            False reports have already cost people precious seconds in their battle against Covid-19. With your help, we can overcome this hurdle. 
            <br/><br/>
            We urge you all to <strong>Unite Against Covid-19 and join us in Spreading Facts, Not Fear</strong>.
        </p>
        <!-- <br/><br/> -->
        <a href="https://forms.gle/v5qH3e3tXwiGPPGb8">
            <button>
                <p><strong>
                    Become a volunteer
                </strong></p>
            </button>
        </a>
        <br/><br/>
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