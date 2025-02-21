<script>
    import { Container, Row, Col, Card, CardBody, CardTitle, CardText } from '@sveltestrap/sveltestrap';
  
    // Sample speaker data
    let speakers = [
      { name: "Dr. John Doe", title: "AI & Robotics Expert", img: "./keyspeaker.jpeg", bio: "Dr. John Doe is a leading expert in AI and robotics, revolutionizing automation." },
      { name: "Jane Smith", title: "Cybersecurity Analyst", img: "/keyspeaker.jpeg", bio: "Jane specializes in cybersecurity and ethical hacking, securing enterprise networks." },
      { name: "Michael Johnson", title: "Cloud Architect", img: "/keyspeaker.jpeg", bio: "Michael is a cloud architect, optimizing cloud solutions for global firms." },
      { name: "Emily Davis", title: "Blockchain Developer", img: "/keyspeaker.jpeg", bio: "Emily is pioneering decentralized applications and smart contracts." }
    ];
  </script>
  
  <Container class="mt-5">
    <h2 class="text-center mb-4">Meet Our Speakers</h2>
    <Row>
      {#each speakers as speaker}
        <Col md="6" lg="3" class="mb-4">
          <Card class="shadow speaker-card">
            <img src={speaker.img} alt={speaker.name} class="card-img-top speaker-img">
            <CardBody class="text-center">
              <CardTitle tag="h4">{speaker.name}</CardTitle>
              <CardText class="text-muted">{speaker.title}</CardText>
              <CardText>{speaker.bio}</CardText>
            </CardBody>
          </Card>
        </Col>
      {/each}
    </Row>
  </Container>
  
  <!-- Styles -->
  <style>
    .speaker-card {
      border-radius: 10px;
      overflow: hidden;
      transition: transform 0.3s ease-in-out;
    }
    
    .speaker-card:hover {
      transform: translateY(-5px);
    }
  
    .speaker-img {
      height: 300px;
      object-fit: cover;
    }
  </style>
  