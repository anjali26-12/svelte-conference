<script>
    import { Container, Table } from '@sveltestrap/sveltestrap';

    // Sample schedule data
    let schedule = [
        { date: "March 10, 2025", time: "10:00 AM - 11:00 AM", topic: "Future of AI & Robotics", speaker: "Dr. John Doe" },
        { date: "March 10, 2025", time: "11:15 AM - 12:15 PM", topic: "Cybersecurity Trends", speaker: "Jane Smith" },
        { date: "March 10, 2025", time: "01:30 PM - 02:30 PM", topic: "Cloud Computing & Scalability", speaker: "Michael Johnson" },
        { date: "March 11, 2025", time: "10:00 AM - 11:00 AM", topic: "Blockchain and Decentralization", speaker: "Emily Davis" },
        { date: "March 11, 2025", time: "11:15 AM - 12:15 PM", topic: "Quantum Computing Advances", speaker: "Dr. Alice Brown" }
    ];
</script>

<Container class="mt-5">
    <h2 class="text-center mb-4">Conference Schedule</h2>
    <Table striped bordered hover responsive class="text-center">
        <thead class="table-dark">
            <tr>
                <th>Date</th>
                <th>Time</th>
                <th>Topic</th>
                <th>Speaker</th>
            </tr>
        </thead>
        <tbody>
            {#each schedule as session}
                <tr>
                    <td>{session.date}</td>
                    <td>{session.time}</td>
                    <td>{session.topic}</td>
                    <td>{session.speaker}</td>
                </tr>
            {/each}
        </tbody>
    </Table>
</Container>

<!-- Styles -->
<style>
    th, td {
        padding: 12px;
    }
    th {
        background-color: #343a40;
        color: white;
    }
</style>
