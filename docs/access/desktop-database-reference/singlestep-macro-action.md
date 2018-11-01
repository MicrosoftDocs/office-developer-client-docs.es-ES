---
title: PasoAPaso (acción de macro)
TOCTitle: SingleStep Macro Action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7bee12bb26c4ed3799fce2481e7d9329aa5d1e61
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868962"
---
# <a name="singlestep-macro-action"></a>PasoAPaso (acción de macro)


**Se aplica a**: Access 2013, Office 2013

Puede usar la acción **PasoAPaso** para pausar la ejecución de una macro y abrir el cuadro de diálogo **Macro paso a paso**.

## <a name="setting"></a>Configuración

La acción **PasoAPaso** no tiene ningún argumento.

## <a name="remarks"></a>Comentarios

  - Use la acción **PasoAPaso** para solucionar los problemas de una macro que no funciona correctamente. Puede agregar la acción **PasoAPaso** a una macro justo antes de una acción de la que sospecha que puede ser la causa del problema. La acción pausa la macro y abre el cuadro de diálogo **Macro paso a paso**. En este cuadro de diálogo se muestra información sobre la actual acción de macro, como el nombre de la macro, las condiciones especificadas, el nombre de la acción, los argumentos y el número de error, si procede. En el cuadro de diálogo, puede hacer clic en **Paso a paso** para ir a la siguiente acción de macro, en **Detener todas las macros** para detener la actual macro y cualquier otra macro que se esté ejecutando, o bien, en **Continuar** para detener el procedimiento paso a paso y reanudar el funcionamiento normal de la macro.

  - La acción **PasoAPaso** es similar a hacer clic en **Paso a paso** del grupo **Herramientas** en la ficha **Diseño** del Generador de macros. La diferencia entre este procedimiento y la ejecución de la acción **PasoAPaso** reside en que al ejecutarse la acción, se puede colocarla dentro de la macro en el lugar exacto donde debe comenzar el paso a paso. De ese modo, no es preciso recorrer todas las acciones anteriores para llegar a la acción que se desea examinar. Por otro lado, cuando se opta por clic en **Paso a paso** en el Generador de macros, es preciso hacerlo antes de ejecutar la macro. En ese caso, el paso a paso comienza con la primera acción de la macro.


> [!NOTE]
> <P>[!NOTA] Si recorre paso a paso una macro hasta el final sin hacer clic en <STRONG>Continuar</STRONG>, el paso a paso estará aún vigente cuando termine la macro. Cualquier macro subsiguiente que ejecute comenzará en modo paso a paso. Para desactivarlo, haga clic en <STRONG>Continuar</STRONG> del cuadro de diálogo <STRONG>Macro paso a paso</STRONG>, o bien, con una macro abierta en la vista Diseño, en la ficha <STRONG>Diseño</STRONG>, en el grupo <STRONG>Herramientas</STRONG>, haga clic en <STRONG>Paso a paso</STRONG> de modo que la opción ya no esté seleccionada.</P>


