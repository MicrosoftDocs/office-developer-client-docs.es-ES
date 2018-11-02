---
title: BuscarRegistroSiguiente (acción de macro)
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0309a72040751aaab994225159fdca6698a189cc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920735"
---
# <a name="findnextrecord-macro-action"></a>BuscarRegistroSiguiente (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **BuscarRegistroSiguiente** para buscar el siguiente registro que cumpla los criterios especificados por la anterior acción **BuscarRegistro** o el valor en el cuadro de diálogo **Buscar y reemplazar** (en la ficha **Inicio**, haga clic en **Buscar**). Puede usar la acción **BuscarRegistroSiguiente** para buscar registros repetidamente. Por ejemplo, para recorrer sucesivamente todos los registros de un cliente concreto.

## <a name="setting"></a>Configuración

La acción **BuscarRegistroSiguiente** no tiene argumentos. La acción **BuscarRegistroSiguiente** busca el siguiente registro que cumpla los criterios establecidos por la acción **BuscarRegistro** o en el cuadro de diálogo **Buscar y reemplazar**. Los argumentos de la acción **BuscarRegistro** se comparten con las opciones del cuadro de diálogo **Buscar y reemplazar**.

Para establecer los criterios de búsqueda, utilice la acción **BuscarRegistro**. Normalmente, se inserta una acción **BuscarRegistro** en una macro y, a continuación, se utiliza la acción **BuscarRegistroSiguiente** para buscar los registros subsiguientes que cumplan los mismos criterios. Para buscar registros sólo cuando se cumple una condición concreta, se puede incluir una expresión condicional en la columna **Condición** de la fila correspondiente a la acción **BuscarRegistroSiguiente**.

## <a name="remarks"></a>Comentarios

Esta acción tiene el mismo efecto que utilizar el botón **Buscar siguiente** del cuadro de diálogo **Buscar y reemplazar**.


> [!NOTE]
> <P>[!NOTA] Si bien la acción <STRONG>BuscarRegistro</STRONG> corresponde al comando <STRONG>Buscar</STRONG> en la ficha <STRONG>Inicio</STRONG> de tablas, consultas y formularios, no corresponde al comando <STRONG>Buscar</STRONG> del menú <STRONG>Edición</STRONG> en la ventana Código. No se puede utilizar la acción <STRONG>BuscarRegistro</STRONG> o <STRONG>BuscarRegistroSiguiente</STRONG> para buscar texto en módulos.</P>




> [!TIP]
> <P>[!SUGERENCIA] Si ha establecido en <STRONG>Sí</STRONG> el valor del argumento <STRONG>Sólo el campo activo</STRONG> de la acción <STRONG>BuscarRegistro</STRONG>, es posible que tenga que utilizar la acción <STRONG>IrAControl</STRONG> para mover el enfoque al control que contiene los datos que está buscando antes de utilizar la acción <STRONG>BuscarRegistroSiguiente</STRONG>.</P>



Si el texto seleccionado actualmente es el mismo que el texto seleccionado en el momento en el que se ejecuta la acción de macro **BuscarRegistroSiguiente**, la búsqueda se inicia inmediatamente después de la selección, en el mismo campo que la selección y en el mismo registro. En caso contrario, la búsqueda se inicia al principio del registro activo. Esto permite buscar múltiples instancias de los mismos criterios de búsqueda que pudieran aparecer en un único registro.

Sin embargo, observe que si usa un botón de comando para ejecutar una macro que contenga la acción **BuscarRegistroSiguiente**, se buscará de forma repetida la primera instancia de los criterios de búsqueda. Este comportamiento se debe a que, al hacer clic en el botón de comando, se quita el enfoque del campo que contiene el valor coincidente. La acción **BuscarRegistroSiguiente** empezará la búsqueda desde el principio del registro. Para evitar este problema, ejecute la macro usando una técnica que no cambie el enfoque, como un botón de una barra de herramientas personalizada o una combinación de teclas definida en una macro AutoKeys. Asimismo, establezca el enfoque de la macro en el campo que contiene los criterios de búsqueda antes de llevar a cabo la acción **BuscarRegistroSiguiente**.

Se produce el mismo comportamiento si se utiliza un botón de comando para ejecutar una macro que contenga la acción **BuscarRegistro** con el argumento **Buscar primero** establecido en **No**.

Para ejecutar la acción **BuscarRegistroSiguiente** desde un módulo de Visual Basic para Aplicaciones, use el método **FindNext** del objeto **DoCmd**.

