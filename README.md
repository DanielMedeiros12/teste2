# teste2
""import { useState } from 'react';
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Table, Thead, Tbody, Tr, Th, Td } from "@chakra-ui/react";
import { motion } from "framer-motion";

export default function App() {
  const [data, setData] = useState([]);
  const [newRow, setNewRow] = useState({ id: '', name: '', email: '' });

  const handleChange = (e) => {
    setNewRow({ ...newRow, [e.target.name]: e.target.value });
  };

  const handleAddRow = () => {
    if (newRow.id && newRow.name && newRow.email) {
      setData([...data, newRow]);
      setNewRow({ id: '', name: '', email: '' });
    }
  };

  return (
    <motion.div initial={{ opacity: 0 }} animate={{ opacity: 1 }} className="p-6">
      <Card className="mb-4">
        <CardContent>
          <input
            type="text"
            placeholder="ID"
            name="id"
            value={newRow.id}
            onChange={handleChange}
            className="mr-2 p-2 border rounded"
          />
          <input
            type="text"
            placeholder="Name"
            name="name"
            value={newRow.name}
            onChange={handleChange}
            className="mr-2 p-2 border rounded"
          />
          <input
            type="text"
            placeholder="Email"
            name="email"
            value={newRow.email}
            onChange={handleChange}
            className="mr-2 p-2 border rounded"
          />
          <Button className="ml-2" onClick={handleAddRow}>
            Adicionar Linha
          </Button>
        </CardContent>
      </Card>

      <Card>
        <CardContent>
          <Table>
            <Thead>
              <Tr>
                <Th>ID</Th>
                <Th>Nome</Th>
                <Th>Email</Th>
              </Tr>
            </Thead>
            <Tbody>
              {data.map((row, index) => (
                <Tr key={index}>
                  <Td>{row.id}</Td>
                  <Td>{row.name}</Td>
                  <Td>{row.email}</Td>
                </Tr>
              ))}
            </Tbody>
          </Table>
        </CardContent>
      </Card>
    </motion.div>
  );
}
""
