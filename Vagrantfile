Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provision "shell", inline: <<-SHELL
  sudo apt update
  echo "INSERT INTO gestion_clinica_veterinaria.pacientes (idPaciente, nombre, especie, raza, edad, dueño) VALUES" >> /home/vagrant/datos_pacientes.sql
  echo "('1', 'Gabriel', 'perro', 'mastin', 15,'Jose')," >> /home/vagrant/datos_pacientes.sql
  echo "('2', 'Pepe', 'gato', 'persa', 10,'Hugo')," >> /home/vagrant/datos_pacientes.sql
  echo "('3', 'Gus', 'pajaro', 'loro', 12,'Daniel');" >> /home/vagrant/datos_pacientes.sql
  SHELL
end
