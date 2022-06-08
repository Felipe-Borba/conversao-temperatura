k3d é tipo um k3s, a proposta disso é ser mais magrinho, perfeito para ambiente dev
se vc tiver usando windows recomendo instalar o k3d e kubectk pelo scoop.sh

tem um bizu que como o k3d roda dentro de um container mesmo criando um node port(para expor a porta) não funciona
sem fazer o port forward no docker ou seja:

```
  $ k3d cluster create <optional-name> -p "30000:30000@loadbalancer"
```

e tem que expecificar o nodePort no manifesto do serviço
