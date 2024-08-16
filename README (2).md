
#  Proyecto numero 1 "Sistema de costos"

Pseudocodigo para generar un sistema de costos


## Autor


- [Matias Zenteno](https://www.github.com/mzentenot)

Algoritmo Proyecto_sistema_de_costos
	//declarar variables del sistema de costos
	Definir PrecioOriginal Como Real
	Definir DescuentoCupon Como Real
	Definir PrecioIVA Como Real
	definir DescuentoxCantidad Como Real
	definir CostoEnvio Como Real 
	Definir PesoPaquete Como Real
	Definir i Como Entero
	definir Pedidos Como Entero
	definir Cantidad,PedidoFinal  Como Entero
	
	Escribir "ingrese producto"
	Leer producto
	
	//Asignacion de valores
	PrecioOriginal<-100
	DescuentoCupon<-0.1
	IVA<-1.12
	DescuentoxCantidad<-0.05
	CostoEnvio<-10
	PesoPaquete<-3
	//Realizar calculo  para cupon de descuento
	DescuentoCupon<-PrecioOriginal-(PrecioOriginal*0.1)
	//Realizar calculo para aplicar el IVA al producto con descuento
	PrecioIVA<-DescuentoCupon
	//Realizar callculo de descuento por cantidad de producto
	DescuentoxCantidad<-PrecioIVA-(PrecioIVA*0.05)
	//Realizar calculo de costo de envio 
	CostoEnvio<-10+(2*3)
	//Realizar calculo del producto final mas el envio de un par
	Preciofinal1<-(PrecioIVA*1)+CostoEnvio
	//Realizar calculo del producto final mas el envio de dos pares
	Preciofinal2<-(DescuentoxCantidad*2)+CostoEnvio
	//Crear un array para realizar lista de pedidos de los productos
	Dimension Pedidos[1]
	//Realizar ingreso de pedidos
	Para i<-1  Hasta 1 Con Paso 1 Hacer
		Escribir "Pedido cliente" i,":"
		Leer pedidos[i]
	FinPara
	//Cantidad de pedidos
	Escribir "La cantidad de pedidos ingresados son:"
	Para i<-1 hasta 1 Con Paso 1 Hacer
		si pedidos[i]<= 1 Entonces
			Escribir pedidos[i]
		FinSi
	FinPara
	//agregar precio y cantidad del producto del pedido por el cliente
	Escribir "Ingrese cantidad de producto solicitado por el cliente:"
	leer Cantidad
	si cantidad>=2 Entonces
		Escribir "Si lleva 2 pares se aplica descuento del 5% donde cada producto queda en un valor de $",DescuentoxCantidad
	SiNo
		Escribir "Si lleva 1 par se aplica descuento cupon 10% y el producto queda en un valor de $", PrecioIVA
	FinSi
	//Calculo final del producto mas el envio
	Escribir "Ingrese cantidad final dell pedido:"
	leer  PedidoFinal
	si PedidoFinal>=2 Entonces
		Escribir "El precio total de 2 pares mas el costo de envio  es  de $",Preciofinal2
	SiNo
		Escribir "El precio total de 1 par mas el costo de encio es de $", Preciofinal1
	FinSi
	//Mostrar valores 
	Escribir "Los valores deglosados de los productos  son:"
	Escribir "El precio original del producto es de = $" PrecioOriginal
	Escribir "El precio del producto con cupon de descuento es de = $", DescuentoCupon
	Escribir "El precio del producto con descuento mas el IVA  agregado es de = $", DescuentoxCantidad
	Escribir "El precio del producto si llevas dos pares, cada producto tiene un valor de = $", DescuentoxCantidad
	Escribir "El costo de envio tiene un valor de = $" CostoEnvio
	Escribir "El precio final de un producto mas el envio es de = $", Preciofinal1
	Escribir "El precio final de dos productos mas elenvio es de = $", Preciofinal2
	
	
	
FinAlgoritmo
## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

