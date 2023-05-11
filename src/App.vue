<style>
form {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

h1 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 30px;
}

label {
  font-size: 1.2rem;
  margin-bottom: 10px;
}

input, select, textarea {
  padding: 8px;
  border: 2px solid #ccc;
  border-radius: 4px;
  font-size: 1.2rem;
  width: 100%;
  margin-bottom: 20px;
}

button {
  background-color: #4CAF50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #3e8e41;
}

input[type="date"] {
  width: 100%;
}

textarea {
  height: 150px;
}

:required {
  border-color: red;
}

:invalid {
  box-shadow: none;
}

:invalid + span::before {
  content: "⚠ ";
  color: red;
  font-size: 1.2rem;
}

:invalid:focus + span::before {
  content: "✖ ";
  color: red;
  font-size: 1.2rem;
}



</style>


<script>function isValidDate(birthdate) {
  const dateRegex = /^\d{4}-\d{2}-\d{2}$/;
  if (!dateRegex.test(birthdate)) {
    return false;
  }
  const parts = birthdate.split("-");
  const year = parseInt(parts[0], 10);
  const month = parseInt(parts[1], 10);
  const day = parseInt(parts[2], 10);
  if (year < 1900 || year > new Date().getFullYear()) {
    return false;
  }
  if (month < 1 || month > 12) {
    return false;
  }
  if (day < 1 || day > 31) {
    return false;
  }
  return true;}
  </script>


  <template>

<title>Formulário de Edição de Perfil</title>
    

        <h1>Formulário de Edição de Perfil</h1>
        
    
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome" required><br><br>
  <label for="email">E-mail:</label>
  <input type="email" id="email" name="email" required><br><br>

  <label for="senha">Senha:</label>
  <input type="password" id="senha" name="senha" required><br><br>

  <label for="confirmacao_senha">Confirmação de Senha:</label>
  <input type="password" id="confirmacao_senha" name="confirmacao_senha" required><br><br>

  <label for="data_nascimento">Data de Nascimento:</label>
  <input type="date" id="data_nascimento" name="data_nascimento" required><br><br>

  <label for="endereco">Endereço:</label>
  <input type="text" id="endereco" name="endereco" required><br><br>

  <label for="cidade">Cidade:</label>
  <input type="text" id="cidade" name="cidade" required><br><br>

  <label for="estado">Estado:</label>
  <select id="estado" name="estado" required>
    <option value="AC">Acre</option>
    <option value="AL">Alagoas</option>
    <option value="AP">Amapá</option>
    <option value="AM">Amazonas</option>
    <option value="BA">Bahia</option>
    <option value="CE">Ceará</option>
    <option value="DF">Distrito Federal</option>
    <option value="ES">Espírito Santo</option>
    <option value="GO">Goiás</option>
    <option value="MA">Maranhão</option>
    <option value="MT">Mato Grosso</option>
    <option value="MS">Mato Grosso do Sul</option>
    <option value="MG">Minas Gerais</option>
    <option value="PA">Pará</option>
    <option value="PB">Paraíba</option>
    <option value="PR">Paraná</option>
    <option value="PE">Pernambuco</option>
    <option value="PI">Piauí</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="RN">Rio Grande do Norte</option>
    <option value="RS">Rio Grande do Sul</option>
    <option value="RO">Rondônia</option>
    <option value="RR">Roraima</option>
    <option value="SC">Santa Catarina</option>
    <option value="SP">São Paulo</option>
    <option value="SE">Sergipe</option>
    <option value="TO">Tocantins</option>
  </select>
  <br>
  <label for="hobbies">Hobbies:</label>
  <input type="text" id="hobbies" name="hobbies"><br><br>
  <label for="linguagens">linguagens de progromação</label>
  <input type="text" id="linguagens" name="linguagens"><br> <label for="biografia">Biografia:</label>
<textarea id="biografia" name="biografia"></textarea><br><br>
  <button type="button" id="salva" name="salvar">Salvar</button>
</template>