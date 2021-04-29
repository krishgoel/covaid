<script>
    // Contributors
	const contributorsDB = (async () => {
		var response = await fetch('https://potion-api.now.sh/table?id=0fb220c98d614169923c9c44240c0327')
		return await response.json()
	})()
</script>


<section>
    <div class="width-restriction" style="width: 70%">
        <h1>About Us</h1>
        <br/>
        <p>
            CovAID is the joint <strong>initiative of 5 students from Sanskriti School, New Delhi</strong>. We have initiated a unified <strong>online platform for smooth and accurate dispersal of information</strong> regarding availability of Covid-19 resources in the National Capital Region. <strong>Verification takes place through direct contact (calls, messages, etc.) that involves pictorial proof</strong>. These verified updates are then posted on the platform at frequent, regular intervals.
            <br/><br/>
            Alongside this, we have also be <strong>created a filter for conveniently searching Twitter updates regarding COVID-19 resources</strong> and availability. The nation has lost many lives due to inaccurate information dispersal. With our initiative, we hope to overcome this hurdle. 
            <br/><br/>
            CovAID is simply a medium to connect the users to suppliers and <strong>does not participate in monetary transactions whatsoever i.e. it is a non-profit organisation</strong>. As the youth of India, we believe it is our duty to help all those that have been affected by the pandemic, whether they're our peers or elders. It is this beautiful country that we will inherit, and we must protect the tree whose roots have snuggled our childhoods.
            <br/><br/>
            <!-- <strong>We're here to help</strong>. Reach out to us via 
            <a href="https://instagram.com/resources_covaid" target="_blank">Instagram</a> or <a href="mailto: covaid000@gmail.com" target="_blank">Email (covaid000@gmail.com)</a>. If you want to speak to us over the phone, DM us on Instagram and we’ll arrange a call with an official. 
            <br/><br/> -->
            Regards,
            <br/>
            Team CovAID
        </p>
        <br/><br/>
        <div class="row">
            <div class="col-3">

                <div class="card">
                    <div class="width-restriction">
                        <h3>Advait Roy</h3>
                        <p>Content Curation</p>
                    </div>
                </div>

                <div class="card">
                    <div class="width-restriction">
                        <h3>Srijan Tripathi</h3>
                        <p>Social Media and Outreach</p>
                    </div>
                </div>

            </div>

            <div class="col-3">

                <div class="card">
                    <div class="width-restriction">
                        <h3>Ishaan Kanudia</h3>
                        <p>Volunteer Affairs</p>
                    </div>
                </div>

                <div class="card">
                    <div class="width-restriction">
                        <h3>Raghav Sarangi</h3>
                        <p>Professional Executive</p>
                    </div>
                </div>

            </div>

            <div class="col-3">

                <div class="card">
                    <div class="width-restriction">
                        <h3>Krish Goel</h3>
                        <p>Tec# $w@ggE₹</p>
                    </div>
                </div>

            </div>
        </div>
        <br/>


        <h2>Team CovAID</h2>
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

        <br/><br/>

        <h3>Disclaimer</h3>
        <p>
            We would like to emphasize that the CovAID team does not take responsibility for the transactions that occur through these leads. No verification process is 100% infallible and there is always a risk for suppliers being fraudulent. We request all users to exercise the requisite discretion to maintain their own safety and security. Rest assured, CovAID is working to the best of its abilities to provide verified, real-time information to those in need.
        </p>
    </div>
</section>

<br/><br/>
        