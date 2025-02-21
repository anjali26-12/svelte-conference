<script>
    import { Container, Row, Col, Card, CardBody } from '@sveltestrap/sveltestrap';

    // List of sponsors
    let sponsors = [
        { name: "TechCorp", logo: "./download.png", website: "https://techcorp.com" },
        { name: "CyberSecure", logo: "./download.png", website: "https://cybersecure.com" },
        { name: "CloudX", logo: "./download.png", website: "https://cloudx.com" },
        { name: "Blockchain Inc.", logo: "./download.png", website: "https://blockchaininc.com" }
    ];
</script>

<Container class="mt-5">
    <h2 class="text-center mb-4">Our Sponsors</h2>
    <Row>
        {#each sponsors as sponsor}
            <Col md="6" lg="3" class="mb-4">
                <Card class="shadow sponsor-card">
                    <a href={sponsor.website} target="_blank" rel="noopener noreferrer">
                        <img src={sponsor.logo} alt={sponsor.name} class="card-img-top sponsor-logo">
                    </a>
                    <CardBody class="text-center">
                        <h5>{sponsor.name}</h5>
                    </CardBody>
                </Card>
            </Col>
        {/each}
    </Row>
</Container>

<!-- Styles -->
<style>
    .sponsor-card {
        border-radius: 10px;
        overflow: hidden;
        transition: transform 0.3s ease-in-out;
        text-align: center;
    }

    .sponsor-card:hover {
        transform: translateY(-5px);
    }

    .sponsor-logo {
        height: 100px;
        object-fit: contain;
        padding: 10px;
    }
</style>

