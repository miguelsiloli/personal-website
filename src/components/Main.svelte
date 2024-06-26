<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Vinted Pipeline",
            icon: "fa-solid fa-cart-shopping",
            href: "https://github.com/miguelsiloli/vinted-pipeline-container",
            href_dashboard: "",
            href_notebooks: "https://miguelsilva-nb.netlify.app/01_vinted_data_engineering/00_intro",
            github_href: "https://github.com/miguelsiloli/vinted-pipeline-container",
            description: "",
            url: "images/prefect.png"
        },
        {
            name: "Vinted Analytics",
            icon: "fa-solid fa-desktop",
            href: "http://16.171.182.134:8502/",
            href_dashboard: "http://16.171.182.134:8502/",
            href_notebooks: "https://miguelsilva-nb.netlify.app/03_vinted_data_science/01_price_prediction",
            github_href: "https://github.com/miguelsiloli/vinted-streamlit-container",
            description: "",
            url: "images/analytics.png"
        },
        {
            name: "Browser Game API",
            icon: "fa-solid fa-gamepad",
            href: "https://github.com/miguelsiloli/tw_bot",
            href_dashboard: "",
            href_notebooks: "",
            github_href: "https://github.com/miguelsiloli/tw_bot",
            description: "",
            url: "images/tribalwars.png"
        },
        {
            name: "Forecasting Tool",
            icon: "fa-solid fa-line-chart",
            href: "https://cpbs-tsa-forecast.streamlit.app/",
            href_dashboard: "https://cpbs-tsa-forecast.streamlit.app",
            href_notebooks: "",
            github_href: "https://github.com/miguelsiloli/CPBS-TSA-Forecast",
            description: "",
            url: "images/forecasting.png"
        }
    ];

    let benefits = [
        {
            metric: "10x",
            name: "An avid sports guy",
            description:
                "My journey in football commenced at the age of five, ignited by my passion for the sport. By the time I reached sixteen, I had the privilege of competing in the national junior championship, marking a pivotal moment in my life. At seventeen I was called to play in the AF Braga district team in inter-regionals play-off and made a short debut in the University of Minho futsal team at 17. After an injury, I decided to give up on the sport but the competitiveness and friendships still remain to this day as an attestement of time!",
            image: ""
            },
        {
            name: "A problem solver",
            description:
                "I am a problem solver often driven by inner curiosity and creativity to seek out-of-the-box solutions to all sorts of problems. Some of my standout skills of engineering are: critical thinking, passion for learning and ability to find out of the box solutions.",
            image: ""
            },
        {
            name: "A genuine friend",
            description:
                "Being genuine is key and it's a non negotiable paramount value of mine. I believe in transparency, truthfulness and effective communication. It is a very polarizing trait as it does help me establish deep relationships, but simultaneously it can make me unlikeable for some.",
            image: ""
            },
        {
            name: "An adaptable coworker",
            description:
                "I am very fluid to fit in organization, both at an interpersonal level and project level. I find this ability of navigate with grace and contribute with meaning a valuable skill in an increasingly changing landscape. Moreover my willingness to learn and take on new responsibilities as well as my interpersonal skills allow me to strive for success.",
            image: ""
            }
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-4 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10 max-w-screen-xl"
        >
            <h2 class="font-semibold text-3xl sm:text-5xl md:text-6xl">
                Miguel Silva
                <br />
                <span class="mt-0">Data Analyst</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My stack includes <span class="poppins text-blue-200">Data Engineering</span> (Airflow, Prefect, Dbt), <span class="poppins text-blue-200">Data Visualization</span> (PowerBI, Flask, Plotly), <span class="poppins text-blue-200">Data Science</span> (Sklearn, Statsmodels, LightGBM)
            </p>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                class="object-cover z-[2] max-h-[35vh] rounded-full"
            />           
        </div>
        <div  class="flex p-0.5 relative max-w-[700px] w-full mx-auto">
            <div
                class="absolute inset-0 overflow-hidden rounded-md flex items-center justify-center"
            >
                <div
                    class="bg-gradient-to-r absolute inset-[-50px]  from-blue-600 to-blue-300 specialSpin"
                />
            </div>
        </div>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Projects
            </h3>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4">
            <Step step={steps[0]}>
                <p>
                    An <strong>ETL pipeline</strong>  on top of Vinted Rest API for Marketing Analytics developed with <strong
                    class="text-blue-200">prefect</strong>, <strong
                    class="text-blue-200">dbt</strong>, <strong
                    class="text-blue-200">requests</strong> and <strong
                    class="text-blue-200">pandas</strong>.       
                </p>
                <p> Deployed using AWS infrastructure (Postgres RDS, S3 image file storage, EC2).</p>
                <p> A project motivated by the increased projections of the rise of second-hand markets and changing patterns of customer behaviors in online shopping.</p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    A dashboard with a <strong>data visualization</strong> component and a <strong>data analytics</strong> components developed <strong
                    class="text-blue-200">streamlit</strong>, <strong
                    class="text-blue-200">sklearn</strong>, <strong
                    class="text-blue-200">LightGBM</strong> and <strong
                    class="text-blue-200">looker studio</strong>.
                </p>
                <p> <strong
                    class="text-blue-500">Main Features:</strong></p>
                <ul>
                    <li>Price regression</li>
                    <li>Product portfolio optimization</li>
                    <li>Customer segmentation</li>
                    <li>Brand segmentation</li>
                  </ul>
                  
            </Step>
            <Step step={steps[2]}>
                <p>
                    A TribalWars <strong>rest API</strong> interface mapping basic user functions to coding functions by HTML parsing using <strong class="text-blue-200">sqlite</strong>, <strong class="text-blue-200">requests</strong>, <strong class="text-blue-200">beatifulsoup</strong> and <strong class="text-blue-200">regex</strong>.
                </p>
                <p> <strong
                    class="text-blue-500">Main Features:</strong></p>
                <ul>
                    <li>Ability to schedule browser actions</li>
                    <li>Ability to perform attacks with +- 15 ms precision</li>
                    <li>SQLite database with user and village statistics</li>
                  </ul>
            </Step>
        <Step step={steps[3]}>
            <p>
                A dynamic dashboard to forecast the sales of a hierarchical dataset using traditional time series analysis solution (case study based on real data).
            </p>
            <p>Built with <strong class="text-blue-200">plotly</strong>, <strong class="text-blue-200">streamlit</strong> and <strong class="text-blue-200">statsmodels</strong>.</p>
        </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 py-4"
        >
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Who am I
            </h3>
        </div>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-20 w-full mx-auto">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8 justify-between">
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>                        
                        <div class="grid grid-cols-3 gap-4">
                            <div class="col-span-2">
                                <p>{benefit.description}</p>
                            </div>
                            
                            <!-- Image column -->
                            <div class="col-span-1">
                                <!-- Place your image here -->
                                <img src={benefit.image} class="w-full rounded-full" />
                            </div>
                        </div>
                        
                    </div>
                </div>
            {/each}
        </div>
             
    </section>
</main>
