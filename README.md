# XML-para-la-SS-con-un-DTD
La tarea consiste en crear un formato de intercambio unificado para distribuir la información personal de los afiliados.
## DTD
Un DTD es una especie de plantilla que obliga a que se cumpla su formato. El DTD propuesto es el siguiente:
```bash
<?xml version="1.0" encoding="iso-8859-1" standalone="yes"
<!DOCTYPE archivoafiliados [
    <!ELEMENT afiliado (#PCDATA)>
        <!ELEMENT DNINIE (#PCDATA)>
        <!ELEMENT nombre (#PCDATA)>
    		<!ATTLIST nombre
    		 nombre1 CDATA #REQUIRED
    		 nombre2 CDATA #IMPLIED
    		 >
       	<!ELEMENT apellidos (#PCDATA)>
       		<!ATTLIST apellidos
       		apellido1 CDATA #REQUIRED
       		apellido2 CDATA #IMPLIED
       		>
        <!ELEMENT fechanacimiento (dia, mes, anio)>
        	<!ELEMENT dia(#PCDATA)>
        	<!ELEMENT mes(#PCDATA)>
        	<!ELEMENT anio(#PCDATA)>
        <!ELEMENT situacionlaboral (En_paro|En_activo|jubilado|Edad_no_laboral)>
        <!ELEMENT listadobajas (causa, fechaInicio, fechaFinal?)>
        	<!ELEMENT causa(#PCDATA)>
        	<!ELEMENT fechaInicio(#PCDATA)>
        	<!ELEMENT fechaFinal(#PCDATA)>
        <!ELEMENT prestacionescobradas (cantidad, fechaInicio, fechaFinal)>
        	<!ELEMENT cantidad(#PCDATA)>
        	<!ELEMENT fechaInicio(#PCDATA)>
        	<!ELEMENT fechaFinal(#PCDATA)>
]>
```
## Resultado final
Al final, juntando el DTD con el XML propuesto, el resultado es:
```bash
<?xml version="1.0" encoding="iso-8859-1" standalone="yes"
<!DOCTYPE archivoafiliados [
    <!ELEMENT afiliado (#PCDATA)>
        <!ELEMENT DNINIE (#PCDATA)>
        <!ELEMENT nombre (#PCDATA)>
    		<!ATTLIST nombre
    		 nombre1 CDATA #REQUIRED
    		 nombre2 CDATA #IMPLIED
    		 >
       	<!ELEMENT apellidos (#PCDATA)>
       		<!ATTLIST apellidos
       		apellido1 CDATA #REQUIRED
       		apellido2 CDATA #IMPLIED
       		>
        <!ELEMENT fechanacimiento (dia, mes, anio)>
        	<!ELEMENT dia(#PCDATA)>
        	<!ELEMENT mes(#PCDATA)>
        	<!ELEMENT anio(#PCDATA)>
        <!ELEMENT situacionlaboral (En_paro|En_activo|jubilado|Edad_no_laboral)>
        <!ELEMENT listadobajas (causa, fechaInicio, fechaFinal?)>
        	<!ELEMENT causa(#PCDATA)>
        	<!ELEMENT fechaInicio(#PCDATA)>
        	<!ELEMENT fechaFinal(#PCDATA)>
        <!ELEMENT prestacionescobradas (cantidad, fechaInicio, fechaFinal)>
        	<!ELEMENT cantidad(#PCDATA)>
        	<!ELEMENT fechaInicio(#PCDATA)>
        	<!ELEMENT fechaFinal(#PCDATA)>
]>

<archivoafiliados>
	<afiliado>
		<DNINIE>""</DNINIE>
		<nombre nombre1="" nombre2="">
		<apellidos apellido1="" apellido2="">
		<fechanacimiento>
			<dia>""</dia>
			<mes>""</mes>
			<anio>""</anio>
		</fechanacimiento>
		<situacionlaboral>
			<en_paro>""</en_paro>
			<En_activo>""</En_activo>
			<jubilado>""</jubilado>
			<Edad_no_laboral>""</Edad_no_laboral>
		</situacionlaboral>
		<listadobajas>
			<causa>""</causa>
			<fechaInicio>""</fechaInicio>
			<fechaFinal>""</fechaFinal>
		</listadobajas>
		<prestacionescobradas>
			<cantidad>""</cantidad>
			<fechaInicio>""</fechaInicio>
			<fechaFinal>""</fechaFinal>
		</prestacionescobradas>
	</afliado>
</archivoafiliados>
```
