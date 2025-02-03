const SUPABASE_URL = "SUA_SUPABASE_URL_AQUI";
const SUPABASE_KEY = "SUA_SUPABASE_CHAVE_ANON_AQUI";
const supabase = supabase.createClient(SUPABASE_URL, SUPABASE_KEY);

document.getElementById("client-form").addEventListener("submit", async function(event) {
    event.preventDefault();

    let codigo = document.getElementById("codigo").value;
    let telefone1 = document.getElementById("telefone1").value;
    let telefone2 = document.getElementById("telefone2").value;
    let razaoSocial = document.getElementById("razaoSocial").value;
    let nomeFantasia = document.getElementById("nomeFantasia").value;
    let notas = document.getElementById("notas").value;

    let cliente = { codigo, telefone1, telefone2, razaoSocial, nomeFantasia, notas };

    // Salvar no LocalStorage
    let clientes = JSON.parse(localStorage.getItem("clientes")) || [];
    clientes.push(cliente);
    localStorage.setItem("clientes", JSON.stringify(clientes));

    // Enviar para o Supabase
    let { error } = await supabase.from("clientes").insert([cliente]);
    if (error) {
        console.error("Erro ao salvar no Supabase:", error);
    }

    carregarClientes();
    this.reset();
});

// Carregar clientes ao abrir a página
function carregarClientes() {
    let lista = document.getElementById("client-list");
    lista.innerHTML = "";

    let clientes = JSON.parse(localStorage.getItem("clientes")) || [];
    clientes.forEach((cliente, index) => {
        let row = lista.insertRow();

        row.innerHTML = `
            <td>${cliente.codigo}</td>
            <td class="cliente-nome" data-notas="${cliente.notas}">${cliente.nomeFantasia}</td>
            <td>${cliente.telefone1}</td>
            <td>${cliente.telefone2}</td>
            <td><button onclick="removerCliente(${index})">🗑</button></td>
        `;
    });

    // Adicionar evento de clique no nome
    document.querySelectorAll(".cliente-nome").forEach(nome => {
        nome.addEventListener("click", function() {
            abrirPopup(this.dataset.notas);
        });
    });
}

// Remover cliente
function removerCliente(index) {
    let clientes = JSON.parse(localStorage.getItem("clientes")) || [];
    clientes.splice(index, 1);
    localStorage.setItem("clientes", JSON.stringify(clientes));
    carregarClientes();
}

// Barra de pesquisa
document.getElementById("search").addEventListener("input", function() {
    let termo = this.value.toLowerCase();
    let clientes = document.querySelectorAll("#client-list tr");

    clientes.forEach(cliente => {
        let nome = cliente.querySelector("td:nth-child(2)").textContent.toLowerCase();
        cliente.style.display = nome.includes(termo) ? "" : "none";
    });
});

// Popup de notas
let popup = document.getElementById("popup");
let popupText = document.getElementById("popup-text");
let close = document.querySelector(".close");

function abrirPopup(notas) {
    popupText.textContent = notas;
    popup.style.display = "block";
}

close.addEventListener("click", function() {
    popup.style.display = "none";
});

// Carregar clientes ao iniciar
carregarClientes();
        // Inicializar
        loadClients();
    </script>
</body>
</html>
