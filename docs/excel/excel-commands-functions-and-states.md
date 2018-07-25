---
title: Comandos, funciones y estados de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815556"
---
# <a name="excel-commands-functions-and-states"></a>Estados, comandos y funciones de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel reconoce dos tipos muy diferentes de funciones agregadas: comandos y funciones.
  
## <a name="commands"></a>Comandos

En Excel, los comandos tienen las siguientes caracter�sticas:
  
- Realizan acciones del mismo modo que los usuarios.
    
- Pueden hacer lo que haga un usuario (sujeto a los l�mites de la interfaz que se use), como modificar la configuraci�n de Excel, abrir, cerrar y editar documentos, iniciar actualizaciones, etc.
    
- Se pueden configurar para que se los llamen cuando se producen determinadas capturas de eventos.
    
- Pueden mostrar cuadros de di�logo e interactuar con el usuario.
    
- Se pueden vincular para controlar los objetos de modo que se les llame al realizar alguna acci�n en ese objeto, como al hacer clic.
    
- Excel nunca los llamar� durante una actualizaci�n.
    
- Las funciones no pueden llamarlos durante una actualizaci�n.
    
## <a name="functions"></a>Funciones

Las funciones de Excel hacen lo siguiente:
  
- Normalmente toman argumentos y siempre devuelven un resultado.
    
- Se pueden introducir en una o varias celdas como parte de una fórmula de Excel.
    
- Se pueden usar en las definiciones de nombre definido.
    
- Se pueden usar en expresiones de umbral y de l�mite de formato condicional.
    
- Los comandos las pueden llamar.
    
- No pueden llamar a comandos.
    
Excel hace una distinci�n m�s entre funciones de hoja de cálculo definidas por el usuario y funciones definidas por el usuario que son dise�adas para trabajar en hojas de macros. Excel no limita las funciones de hoja de macros definidas por el usuario que solo se van a usar en hojas de macros: estas funciones se pueden usar en cualquier lugar en el que se pueda usar una función de hoja de cálculo normal.
  
### <a name="worksheet-functions"></a>Funciones de hoja de cálculo

Lo siguiente es verdadero de funciones de hoja de cálculo de Excel:
  
- No pueden acceder a las funciones de información de hojas de macros.
    
- No pueden obtiener los valores de las celdas no actualizadas.
    
- Se pueden escribir y registrar como seguros para subprocesos a partir de Excel 2007.
    
### <a name="macro-sheet-functions"></a>Funciones de hoja de macros

Lo siguiente es verdadero de funciones de hoja de macros de Excel:
  
- Pueden acceder a las funciones de información de hojas de macros.
    
- Pueden obtener los valores de las celdas no actualizadas, incluidos los valores de las celdas de llamada.
    
- No se consideran inicios seguros para subprocesos en Excel 2007.
    
C�mo trata Excel a una función definida por el usuario (UDF), qu� permite que haga la función y c�mo actualiza la función se determina al registrar la función. Si una función est� registrada como una función de hoja de cálculo e intenta hacer algo que solo puede hacer una función de hoja de macros, la operaci�n dar� un error. A partir de Excel 2007, si una función de hoja de cálculo registrada como segura para subprocesos intenta llamar a una función de hoja de macros, la operaci�n dar� un error.
  
Excel trata los UDF de Microsoft Visual Basic para aplicaciones (VBA) como funciones equivalentes de hoja de macros, en las que pueden acceder a la información del �rea de trabajo y al valor de las celdas no actualizadas, y no se consideran como seguros para subprocesos a partir de Excel 2007.
  
## <a name="excel-states"></a>Estados de Excel

Excel puede estar en uno de varios estados en un momento dado, dependiendo de las acciones del usuario, un proceso externo, un evento capturado que ejecuta una macro o un evento de mantenimiento programado de Excel, como **Autosave**.
  
Los estados que experimentan los usuarios son los siguientes:
  
- **Estado Listo:** no se ejecutan comandos o macros. No se muestran cuadros de di�logo. No se editan celdas y el usuario no est� en medio de una operaci�n de cortar, y copiar y pegar. Ning�n objeto insertado tiene el foco. 
    
- **Modo Editar:** el usuario empieza a escribir los caracteres de entrada v�lidos en una celda desbloqueada o desprotegida, o presiona **F2** en una o varias celdas desbloqueadas o desprotegidas. 
    
- **Modo Cortar/Copiar y pegar:** el usuario corta o copia una celda o un rango de celdas y a�n no las ha pegado, o las ha pegado con el cuadro de di�logo de pegado especial que permite varias operaciones de pegado. 
    
- **Modo Se�alar:** el usuario edita una fórmula y selecciona celdas cuyas direcciones se agregan a la fórmula que se edita. 
    
El usuario puede borrar los modos de Editar, Se�alar y Cortar/Copiar presionando la tecla **ESC**, que devuelve a Excel a su estado listo. Otros eventos pueden borrar estos estados, como los siguientes: 
  
- El usuario abre un cuadro de di�logo integrado.
    
- El usuario inicia una actualizaci�n.
    
- El usuario ejecuta un comando.
    
- Excel realiza una operaci�n **Autosave**. 
    
- Se captura un evento de temporizador.
    
El �ltimo ejemplo es importante para los desarrolladores de complementos. Debe tener en cuenta el impacto de la facilidad de uso normal de Excel, donde se configuran y ejecutan capturas de eventos de temporizador. Cuando se trata de una parte importante de funcionalidad del complemento, debe proporcionar a los usuarios un modo sencillo para suspenderlo, para que puedan cortar/copiar y pegar normalmente cuando sea necesario.
  
## <a name="see-also"></a>Vea también



[Conceptos de programación de Excel](excel-programming-concepts.md)
  
[Saltos de usuario de coordinaci�n de operaciones largas](permitting-user-breaks-in-lengthy-operations.md)

