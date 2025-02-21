<script>
    import { Container, Row, Col, Card, CardBody } from '@sveltestrap/sveltestrap';
</script>

<Container class="mt-5">
    <h2 class="text-center mb-4">About the Conference</h2>
    <Row class="align-items-center">
        <Col md="6">
            <img src="./hero-bg.webp" alt="Conference Image" class="about-image">
        </Col>
        <Col md="6">
            <Card class="shadow about-card">
                <CardBody>
                    <h4>Welcome to the Future of Technology</h4>
                    <p>
                        The <strong>Global Tech Conference 2025</strong> brings together industry leaders, 
                        researchers, and professionals to discuss the latest advancements in 
                        <em>Artificial Intelligence, Cybersecurity, Cloud Computing, and Blockchain</em>.  
                    </p>
                    <p>
                        Join us for an immersive experience filled with keynote speeches, panel discussions, 
                        and networking opportunities. Explore the innovations shaping our future!
                    </p>
                </CardBody>
            </Card>
        </Col>
    </Row>
</Container>

<!-- Styles -->
<style>
    .about-image {
        width: 100%;
        height: auto;
        border-radius: 10px;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
    }

    .about-card {
        border-radius: 10px;
        padding: 20px;
        transition: transform 0.3s ease-in-out;
    }

    .about-card:hover {
        transform: translateY(-5px);
    }
</style>
