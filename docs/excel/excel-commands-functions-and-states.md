---
title: Comandos, funciones y estados de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716239"
---
# <a name="excel-commands-functions-and-states"></a>Estados, comandos y funciones de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel reconoce dos tipos muy diferentes de funciones agregadas: comandos y funciones.
  
## <a name="commands"></a>Comandos

En Excel, los comandos tienen las siguientes características:
  
- Realizan acciones del mismo modo que los usuarios.
    
- Pueden hacer lo que haga un usuario (sujeto a los límites de la interfaz que se use), como modificar la configuración de Excel, abrir, cerrar y editar documentos, iniciar actualizaciones, etc.
    
- Se pueden configurar para que se los llamen cuando se producen determinadas capturas de eventos.
    
- Pueden mostrar cuadros de diálogo e interactuar con el usuario.
    
- Se pueden vincular para controlar los objetos de modo que se les llame al realizar alguna acción en ese objeto, como al hacer clic.
    
- Excel nunca los llamará durante una actualización.
    
- Las funciones no pueden llamarlos durante una actualización.
    
## <a name="functions"></a>Funciones

Las funciones de Excel hacen lo siguiente:
  
- Normalmente toman argumentos y siempre devuelven un resultado.
    
- Se pueden introducir en una o varias celdas como parte de una fórmula de Excel.
    
- Se pueden usar en las definiciones de nombre definido.
    
- Se pueden usar en expresiones de umbral y de límite de formato condicional.
    
- Los comandos las pueden llamar.
    
- No pueden llamar a comandos.
    
Excel hace una distinción más entre funciones de hoja de cálculo definidas por el usuario y funciones definidas por el usuario que son diseñadas para trabajar en hojas de macros. Excel no limita las funciones de hoja de macros definidas por el usuario que solo se van a usar en hojas de macros: estas funciones se pueden usar en cualquier lugar en el que se pueda usar una función de hoja de cálculo normal.
  
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
    
Cómo trata Excel a una función definida por el usuario (UDF), qué permite que haga la función y cómo actualiza la función se determina al registrar la función. Si una función está registrada como una función de hoja de cálculo e intenta hacer algo que solo puede hacer una función de hoja de macros, la operación dará un error. A partir de Excel 2007, si una función de hoja de cálculo registrada como segura para subprocesos intenta llamar a una función de hoja de macros, la operación dará un error.
  
Excel trata los UDF de Microsoft Visual Basic para aplicaciones (VBA) como funciones equivalentes de hoja de macros, en las que pueden acceder a la información del área de trabajo y al valor de las celdas no actualizadas, y no se consideran como seguros para subprocesos a partir de Excel 2007.
  
## <a name="excel-states"></a>Estados de Excel

Excel puede estar en uno de varios estados en un momento dado, dependiendo de las acciones del usuario, un proceso externo, un evento capturado que ejecuta una macro o un evento de mantenimiento programado de Excel, como **Autosave**.
  
Los estados que experimentan los usuarios son los siguientes:
  
- **Estado Listo:** no se ejecutan comandos o macros. No se muestran cuadros de diálogo. No se editan celdas y el usuario no está en medio de una operación de cortar, y copiar y pegar. Ningún objeto insertado tiene el foco. 
    
- **Modo Editar:** el usuario empieza a escribir los caracteres de entrada válidos en una celda desbloqueada o desprotegida, o presiona **F2** en una o varias celdas desbloqueadas o desprotegidas. 
    
- **Modo Cortar/Copiar y pegar:** el usuario corta o copia una celda o un rango de celdas y aún no las ha pegado, o las ha pegado con el cuadro de diálogo de pegado especial que permite varias operaciones de pegado. 
    
- **Modo Señalar:** el usuario edita una fórmula y selecciona celdas cuyas direcciones se agregan a la fórmula que se edita. 
    
El usuario puede borrar los modos de Editar, Señalar y Cortar/Copiar presionando la tecla **ESC**, que devuelve a Excel a su estado listo. Otros eventos pueden borrar estos estados, como los siguientes: 
  
- El usuario abre un cuadro de diálogo integrado.
    
- El usuario inicia una actualización.
    
- El usuario ejecuta un comando.
    
- Excel realiza una operación **Autosave**. 
    
- Se captura un evento de temporizador.
    
El último ejemplo es importante para los desarrolladores de complementos. Debe tener en cuenta el impacto de la facilidad de uso normal de Excel, donde se configuran y ejecutan capturas de eventos de temporizador. Cuando se trata de una parte importante de funcionalidad del complemento, debe proporcionar a los usuarios un modo sencillo para suspenderlo, para que puedan cortar/copiar y pegar normalmente cuando sea necesario.
  
## <a name="see-also"></a>Vea también



[Conceptos de programación de Excel](excel-programming-concepts.md)
  
[Permitir interrupciones de usuarios en operaciones largas](permitting-user-breaks-in-lengthy-operations.md)

