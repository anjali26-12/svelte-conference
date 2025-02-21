<script>
    import { Container, Row, Col, Form, FormGroup, Label, Input, Button } from '@sveltestrap/sveltestrap';

    let name = "";
    let email = "";
    let message = "";

    function submitForm() {
        alert(`Message Sent!\nName: ${name}\nEmail: ${email}\nMessage: ${message}`);
        name = "";
        email = "";
        message = "";
    }
</script>

<Container class="mt-5">
    <h2 class="text-center mb-4">Contact Us</h2>
    
    <Row>
        <!-- Contact Form -->
        <Col md="6">
            <Form on:submit ={submitForm} class="shadow p-4 contact-form">
                <FormGroup>
                    <Label for="name">Name</Label>
                    <Input type="text" id="name" bind:value={name} required />
                </FormGroup>
                <FormGroup>
                    <Label for="email">Email</Label>
                    <Input type="email" id="email" bind:value={email} required />
                </FormGroup>
                <FormGroup>
                    <Label for="message">Message</Label>
                    <Input type="textarea" id="message" bind:value={message} required />
                </FormGroup>
                <Button color="primary" block>Send Message</Button>
            </Form>
        </Col>

        <!-- Social Media Links -->
        <Col md="6" class="text-center">
            <h4>Follow Us</h4>
            <p>Stay connected with us on social media</p>
            <a href="https://facebook.com" target="_blank" class="social-icon">
                <img src="/icons/facebook.svg" alt="Facebook">
            </a>
            <a href="https://twitter.com" target="_blank" class="social-icon">
                <img src="/icons/twitter.svg" alt="Twitter">
            </a>
            <a href="https://linkedin.com" target="_blank" class="social-icon">
                <img src="/icons/linkedin.svg" alt="LinkedIn">
            </a>
        </Col>
    </Row>
</Container>

<!-- Styles -->
<style>
    .contact-form {
        border-radius: 10px;
        background: #fff;
    }

    .social-icon img {
        width: 40px;
        margin: 10px;
        transition: transform 0.3s ease-in-out;
    }

    .social-icon img:hover {
        transform: scale(1.1);
    }
</style>
