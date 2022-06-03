# Listar_Tarefas_PHP
<p> Listar_Tarefas_PHP _Com MySql este programa foi construido com base na linguagem PHP em conjunto com javascript e Bootstrap </p>
<h1> Como usar esta aplicação ? </h1>
<p> para que possa ser possível ver esta aplicação no front end e necessário  ter o XAMPP instalado em sua maquina, em Conjunto com o apache e p MySQL </p>
<h1> Banco de dados </h1>
<p> So sera possível visualizar  esta aplicação  e suas funcionalidades  atraves da criação  de um banco de dados em suas máquina </p>
<h1> Criação das tabelas </h1>
<p> Por favor copie estes códigos para a criação da tabela em sua maquina em sua máquina </p>
<hr>
<p>
 create table tb_status(
	id int not null primary key auto_increment,
    status varchar(25) not null
);

insert into tb_status(status)values('pendente');
insert into tb_status(status)values('realizado');

create table tb_tarefas(
	id int not null primary key auto_increment,
    id_status int not null default 1,
    foreign key(id_status) references tb_status(id),
	tarefa text not null,
    data_cadastrado datetime not null default current_timestamp
)
</p>
<h2> Criação do banco de dados </h2>
<p> Crie um banco de dados para a conexão da aplicação </p>
<h4> Cuidado  com a segurança </h4>
<p> esta aplicação foi construida para evitar possíveis  invasões então separe os arquivos publicos do privado </p>

 
