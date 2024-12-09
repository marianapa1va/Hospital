# Sistema de Gerenciamento de Consultas para Hospital

🚧 **ATENÇÃO: Este projeto está em desenvolvimento!** 🚧  

Algumas funcionalidades ainda estão sendo implementadas. Sinta-se à vontade para explorar, mas esteja ciente de que o projeto não está totalmente funcional.  

**Descrição**

Este projeto utiliza o MongoDB como banco de dados para gerenciar consultas, médicos, pacientes e informações relacionadas ao funcionamento de um hospital. O objetivo é informatizar o registro de consultas e receitas, proporcionando eficiência e organização à área clínica.

# Funcionalidades do Sistema

-Cadastro de médicos

-Armazena dados pessoais e especialidades (ex.: pediatria, clínica geral, etc.).
Cadastro de pacientes

-Registra informações como nome, documentos, contato e convênios.
Gestão de convênios

-Inclui dados do convênio, como nome, CNPJ e tempo de carência.
Registro de consultas

-Mantém informações de data, hora, médico responsável, paciente, valor/convênio e especialidade buscada.
Controle de receitas médicas

-Permite registrar medicamentos prescritos, quantidade e instruções de uso.

# Estrutura do Banco de Dados

O sistema utiliza coleções do MongoDB para armazenar os dados.

**Coleções e Estrutura**

1.Médicos
```js
db.pacientes.insertMany([
    {
      "nome": "Anitta Lima Ferreira",
      "data_nascimento": ISODate("1993-05-14T00:00:00Z"),
      "endereco": "Rua das Flores, 123 - São Paulo, SP",
      "telefone": "(11) 98765-4321",
      "email": "anitta.ferreira@gmail.com",
      "documentos": {
        "CPF": "123.456.789-09",
        "RG": "12.345.678-9"
      },
      "convenio": false
    },
    {
      "nome": "Benício Carvalho da Assunção",
      "data_nascimento": ISODate("1988-11-20T00:00:00Z"),
      "endereco": "Av. Brasil, 456 - Rio de Janeiro, RJ",
      "telefone": "(21) 96543-2198",
      "email": "benicio.assuncao@gmail.com",
      "documentos": {
        "CPF": "987.654.321-00",
        "RG": "98.765.432-1"
      },
      "convenio": {
        "nome": "Saúde Mais",
        "CNPJ": "12.345.678/0001-90",
        "carencia": 30
      }
    },
    {
      "nome": "Carlos Eduardo de Santana Rocha",
      "data_nascimento": ISODate("1975-09-02T00:00:00Z"),
      "endereco": "Rua Almeida, 789 - Salvador, BA",
      "telefone": "(71) 91234-5678",
      "email": "carlos.santana@gmail.com",
      "documentos": {
        "CPF": "159.753.468-20",
        "RG": "45.678.912-3"
      },
      "convenio": {
        "nome": "Vida Leve",
        "CNPJ": "34.567.890/0001-12",
        "carencia": 15
      }
    },
    {
      "nome": "Dandara Maria da Silva",
      "data_nascimento": ISODate("1990-07-18T00:00:00Z"),
      "endereco": "Av. Paulista, 1000 - São Paulo, SP",
      "telefone": "(11) 97654-3210",
      "email": "dandara.silva@gmail.com",
      "documentos": {
        "CPF": "357.159.246-80",
        "RG": "67.890.123-4"
      },
      "convenio": {
        "nome": "Cuidar Bem",
        "CNPJ": "56.789.012/0001-34",
        "carencia": 10
      }
    },
    {
      "nome": "Erivaldo da Penha Silva",
      "data_nascimento": ISODate("1982-03-25T00:00:00Z"),
      "endereco": "Rua das Palmeiras, 555 - Recife, PE",
      "telefone": "(81) 95432-1098",
      "email": "erivaldo.silva@gmail.com",
      "documentos": {
        "CPF": "741.852.963-30",
        "RG": "23.456.789-5"
      },
      "convenio": {
        "nome": "Saúde Total",
        "CNPJ": "78.901.234/0001-56",
        "carencia": 20
      }
    },
    {
      "nome": "Felipa Alves Ribeiro",
      "data_nascimento": ISODate("1985-10-12T00:00:00Z"),
      "endereco": "Av. Independência, 222 - Porto Alegre, RS",
      "telefone": "(51) 98765-4321",
      "email": "felipa.ribeiro@gmail.com",
      "documentos": {
        "CPF": "852.741.369-70",
        "RG": "89.012.345-6"
      },
      "convenio": {
        "nome": "Bem Estar",
        "CNPJ": "12.123.456/0001-78",
        "carencia": 25
      }
    },
    {
      "nome": "Gustavo Oliveira Martins",
      "data_nascimento": ISODate("1991-08-05T00:00:00Z"),
      "endereco": "Rua do Comércio, 333 - Belo Horizonte, MG",
      "telefone": "(31) 95678-1234",
      "email": "gustavo.martins@gmail.com",
      "documentos": {
        "CPF": "963.258.147-50",
        "RG": "90.123.456-0"
      },
      "convenio": {
        "nome": "Plano Fácil",
        "CNPJ": "34.567.890/0001-56",
        "carencia": 40
      }
    },
    {
      "nome": "Henrique Duarte de Sá",
      "data_nascimento": ISODate("1994-02-27T00:00:00Z"),
      "endereco": "Av. Central, 987 - Curitiba, PR",
      "telefone": "(41) 98765-4321",
      "email": "henrique.sa@gmail.com",
      "documentos": {
        "CPF": "654.789.321-10",
        "RG": "12.345.678-9"
      },
      "convenio": {
        "nome": "Saúde em Dia",
        "CNPJ": "56.789.012/0001-98",
        "carencia": 35
      }
    },
    {
      "nome": "Ivete Sangalo da Silva",
      "data_nascimento": ISODate("1987-12-11T00:00:00Z"),
      "endereco": "Rua Vitória, 654 - Fortaleza, CE",
      "telefone": "(85) 91234-5678",
      "email": "ivete.silva@gmail.com",
      "documentos": {
        "CPF": "123.456.789-00",
        "RG": "23.456.789-5"
      },
      "convenio": false
    },
    {
        "nome": "Juliana Gonçalves de Piva",
        "data_nascimento": ISODate("1989-04-22T00:00:00Z"),
        "endereco": "Rua São João, 321 - São Paulo, SP",
        "telefone": "(11) 96876-5432",
        "email": "juliana.piva@gmail.com",
        "documentos": {
          "CPF": "321.654.987-60",
          "RG": "56.789.012-8"
        },
        "convenio": {
          "nome": "Saúde Fácil",
          "CNPJ": "78.123.456/0001-34",
          "carencia": 15
        }
      },
      {
        "nome": "Kauane Sousa Vieira",
        "data_nascimento": ISODate("1992-07-17T00:00:00Z"),
        "endereco": "Avenida Brasil, 432 - Florianópolis, SC",
        "telefone": "(48) 98432-1098",
        "email": "kauane.vieira@gmail.com",
        "documentos": {
          "CPF": "654.987.321-00",
          "RG": "45.678.910-1"
        },
        "convenio": {
          "nome": "Vida Boa",
          "CNPJ": "12.345.678/0001-90",
          "carencia": 20
        }
      },
      {
        "nome": "Leandro Martins de Ferreira",
        "data_nascimento": ISODate("1980-06-05T00:00:00Z"),
        "endereco": "Rua Nova, 890 - Campinas, SP",
        "telefone": "(19) 99123-4567",
        "email": "leandro.ferreira@gmail.com",
        "documentos": {
          "CPF": "987.654.321-09",
          "RG": "78.901.234-5"
        },
        "convenio": {
          "nome": "Saúde Ideal",
          "CNPJ": "34.567.890/0001-23",
          "carencia": 18
        }
      },
      {
        "nome": "Maria Carvalho de Paiva",
        "data_nascimento": ISODate("1978-12-11T00:00:00Z"),
        "endereco": "Avenida Santos, 456 - Rio de Janeiro, RJ",
        "telefone": "(21) 96789-1234",
        "email": "maria.paiva@gmail.com",
        "documentos": {
          "CPF": "741.258.963-11",
          "RG": "90.123.456-7"
        },
        "convenio": {
          "nome": "Plano Saúde",
          "CNPJ": "12.345.678/0001-01",
          "carencia": 22
        }
      },
      {
        "nome": "Nycolas Barbosa Gonçalves",
        "data_nascimento": ISODate("1996-08-23T00:00:00Z"),
        "endereco": "Rua dos Lirios, 789 - Salvador, BA",
        "telefone": "(71) 95543-8765",
        "email": "nycolas.goncalves@gmail.com",
        "documentos": {
          "CPF": "987.321.654-22",
          "RG": "23.456.789-1"
        },
        "convenio": {
          "nome": "MedicoSeguro",
          "CNPJ": "34.567.890/0001-45",
          "carencia": 25
        }
      },
      {
        "nome": "Otávio Oliveira Barbosa",
        "data_nascimento": ISODate("1983-01-14T00:00:00Z"),
        "endereco": "Rua das Palmeiras, 666 - Belo Horizonte, MG",
        "telefone": "(31) 93287-6543",
        "email": "otavio.barbosa@gmail.com",
        "documentos": {
          "CPF": "654.987.123-44",
          "RG": "34.567.890-2"
        },
        "convenio": {
          "nome": "Mais Saúde",
          "CNPJ": "23.456.789/0001-78",
          "carencia": 30
        }
      }
  ]);
  
```

2.Pacientes
```js
db.pacientes.insertMany([
    {
      "nome": "Anitta Lima Ferreira",
      "data_nascimento": ISODate("1993-05-14T00:00:00Z"),
      "endereco": "Rua das Flores, 123 - São Paulo, SP",
      "telefone": "(11) 98765-4321",
      "email": "anitta.ferreira@gmail.com",
      "documentos": {
        "CPF": "123.456.789-09",
        "RG": "12.345.678-9"
      },
      "convenio": false
    },
    {
      "nome": "Benício Carvalho da Assunção",
      "data_nascimento": ISODate("1988-11-20T00:00:00Z"),
      "endereco": "Av. Brasil, 456 - Rio de Janeiro, RJ",
      "telefone": "(21) 96543-2198",
      "email": "benicio.assuncao@gmail.com",
      "documentos": {
        "CPF": "987.654.321-00",
        "RG": "98.765.432-1"
      },
      "convenio": false
    },
    {
      "nome": "Carlos Eduardo de Santana Rocha",
      "data_nascimento": ISODate("1975-09-02T00:00:00Z"),
      "endereco": "Rua Almeida, 789 - Salvador, BA",
      "telefone": "(71) 91234-5678",
      "email": "carlos.santana@gmail.com",
      "documentos": {
        "CPF": "159.753.468-20",
        "RG": "45.678.912-3"
      },
      "convenio": {
        "nome": "Vida Leve",
        "CNPJ": "34.567.890/0001-12",
        "carencia": 15
      }
    },
    {
      "nome": "Dandara Maria da Silva",
      "data_nascimento": ISODate("1990-07-18T00:00:00Z"),
      "endereco": "Av. Paulista, 1000 - São Paulo, SP",
      "telefone": "(11) 97654-3210",
      "email": "dandara.silva@gmail.com",
      "documentos": {
        "CPF": "357.159.246-80",
        "RG": "67.890.123-4"
      },
      "convenio": {
        "nome": "Cuidar Bem",
        "CNPJ": "56.789.012/0001-34",
        "carencia": 10
      }
    },
    {
      "nome": "Erivaldo da Penha Silva",
      "data_nascimento": ISODate("1982-03-25T00:00:00Z"),
      "endereco": "Rua das Palmeiras, 555 - Recife, PE",
      "telefone": "(81) 95432-1098",
      "email": "erivaldo.silva@gmail.com",
      "documentos": {
        "CPF": "741.852.963-30",
        "RG": "23.456.789-5"
      },
      "convenio": {
        "nome": "Saúde Total",
        "CNPJ": "78.901.234/0001-56",
        "carencia": 20
      }
    },
    {
      "nome": "Felipa Alves Ribeiro",
      "data_nascimento": ISODate("1985-10-12T00:00:00Z"),
      "endereco": "Av. Independência, 222 - Porto Alegre, RS",
      "telefone": "(51) 98765-4321",
      "email": "felipa.ribeiro@gmail.com",
      "documentos": {
        "CPF": "852.741.369-70",
        "RG": "89.012.345-6"
      },

      "convenio": false
    },
    {
      "nome": "Gustavo Oliveira Martins",
      "data_nascimento": ISODate("1991-08-05T00:00:00Z"),
      "endereco": "Rua do Comércio, 333 - Belo Horizonte, MG",
      "telefone": "(31) 95678-1234",
      "email": "gustavo.martins@gmail.com",
      "documentos": {
        "CPF": "963.258.147-50",
        "RG": "90.123.456-0"
      },
      "convenio": false
    },
    {
      "nome": "Henrique Duarte de Sá",
      "data_nascimento": ISODate("1994-02-27T00:00:00Z"),
      "endereco": "Av. Central, 987 - Curitiba, PR",
      "telefone": "(41) 98765-4321",
      "email": "henrique.sa@gmail.com",
      "documentos": {
        "CPF": "654.789.321-10",
        "RG": "12.345.678-9"
      },
      "convenio": {
        "nome": "Saúde em Dia",
        "CNPJ": "56.789.012/0001-98",
        "carencia": 35
      }
    },
    {
      "nome": "Ivete Sangalo da Silva",
      "data_nascimento": ISODate("1987-12-11T00:00:00Z"),
      "endereco": "Rua Vitória, 654 - Fortaleza, CE",
      "telefone": "(85) 91234-5678",
      "email": "ivete.silva@gmail.com",
      "documentos": {
        "CPF": "123.478.789-00",
        "RG": "23.456.789-5"
      },
      "convenio": false
    },
    {
        "nome": "Juliana Gonçalves de Piva",
        "data_nascimento": ISODate("1989-04-22T00:00:00Z"),
        "endereco": "Rua São João, 321 - São Paulo, SP",
        "telefone": "(11) 96876-5432",
        "email": "juliana.piva@gmail.com",
        "documentos": {
          "CPF": "321.654.987-60",
          "RG": "56.789.012-8"
        },
        "convenio": {
          "nome": "Saúde Fácil",
          "CNPJ": "78.123.456/0001-34",
          "carencia": 15
        }
      },
      {
        "nome": "Kauane Sousa Vieira",
        "data_nascimento": ISODate("1992-07-17T00:00:00Z"),
        "endereco": "Avenida Brasil, 432 - Florianópolis, SC",
        "telefone": "(48) 98432-1098",
        "email": "kauane.vieira@gmail.com",
        "documentos": {
          "CPF": "654.987.321-00",
          "RG": "45.678.910-1"
        },
        "convenio": {
          "nome": "Vida Boa",
          "CNPJ": "12.345.678/0001-90",
          "carencia": 20
        }
      },
      {
        "nome": "Leandro Martins de Ferreira",
        "data_nascimento": ISODate("1980-06-05T00:00:00Z"),
        "endereco": "Rua Nova, 890 - Campinas, SP",
        "telefone": "(19) 99123-4567",
        "email": "leandro.ferreira@gmail.com",
        "documentos": {
          "CPF": "987.654.321-09",
          "RG": "78.901.234-5"
        },
        "convenio": {
          "nome": "Saúde Ideal",
          "CNPJ": "34.567.890/0001-23",
          "carencia": 18
        }
      },
      {
        "nome": "Maria Carvalho de Paiva",
        "data_nascimento": ISODate("1978-12-11T00:00:00Z"),
        "endereco": "Avenida Santos, 456 - Rio de Janeiro, RJ",
        "telefone": "(21) 96789-1234",
        "email": "maria.paiva@gmail.com",
        "documentos": {
          "CPF": "741.258.963-11",
          "RG": "90.123.456-7"
        },
        "convenio": {
          "nome": "Plano Saúde",
          "CNPJ": "12.345.678/0001-01",
          "carencia": 22
        }
      },
      {
        "nome": "Nycolas Barbosa Gonçalves",
        "data_nascimento": ISODate("1996-08-23T00:00:00Z"),
        "endereco": "Rua dos Lirios, 789 - Salvador, BA",
        "telefone": "(71) 95543-8765",
        "email": "nycolas.goncalves@gmail.com",
        "documentos": {
          "CPF": "987.321.654-22",
          "RG": "23.456.789-1"
        },
        "convenio": {
          "nome": "MedicoSeguro",
          "CNPJ": "34.567.890/0001-45",
          "carencia": 25
        }
      },
      {
        "nome": "Otávio Oliveira Barbosa",
        "data_nascimento": ISODate("1983-01-14T00:00:00Z"),
        "endereco": "Rua das Palmeiras, 666 - Belo Horizonte, MG",
        "telefone": "(31) 93287-6543",
        "email": "otavio.barbosa@gmail.com",
        "documentos": {
          "CPF": "654.987.123-44",
          "RG": "34.567.890-2"
        },
        "convenio": false
        }
        ]);
  
```
