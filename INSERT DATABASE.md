CREATE TABLE descuento(

  	 id_descuento INT AUTO_INCREMENT PRIMARY KEY,

  	 tipo_descuento ENUM('PORCENTAJE','MONTO FIJO'),

   condiciones TEXT,

  	 porcentaje INT,

  	 estado ENUM('ACTIVO','INACTIVO')

   );

ALTER TABLE factura

  	 ADD COLUMN impuesto double;

ALTER TABLE factura

  	 ADD COLUMN descuento int;

INSERT INTO descuento (tipo_descuento, condiciones, porcentaje, estado) VALUES ('PORCENTAJE', 'SE DA POR COMPRAS MAYORES A 20$', 5, 'ACTIVO');

INSERT INTO descuento (tipo_descuento, condiciones, porcentaje, estado) VALUES ('MONTO FIJO', 'SE DA POR SER CLIENTE GOLD', 10, 'ACTIVO');

INSERT INTO descuento (tipo_descuento, condiciones, porcentaje, estado) VALUES ('PORCENTAJE', 'SE DA POR COMPRAS EN NAVIDAD', 3, 'ACTIVO');

INSERT INTO descuento (tipo_descuento, condiciones, porcentaje, estado) VALUES ('PORCENTAJE', 'SE DA POR COMPRAS LOS VIERNES', 5, 'ACTIVO');

INSERT INTO descuento (tipo_descuento, condiciones, porcentaje, estado) VALUES ('MONTO FIJO', 'SE DA POR COMPRAS MAYORES A 1500$', 10, 'ACTIVO');