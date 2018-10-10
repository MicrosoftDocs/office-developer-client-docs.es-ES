---
title: Conjunto de formulario, informe y propiedades de control
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484508"
---
# <a name="set-form-report-and-control-properties"></a>Conjunto de formulario, informe y propiedades de control

**Se aplica a**: Access 2013 | Office 2013

Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado. Las propiedades se examinan y se cambian usando la hoja de propiedades, una macro, o Visual Basic.

## <a name="set-properties"></a>Establecer las propiedades

1. En la vista Diseño del formulario o vista Diseño del informe, seleccione el control, sección, formulario o informe para el que desea establecer la propiedad. Puede seleccionar:
    
   - Uno o más controles. Para seleccionar controles múltiples, se puede hacer clic en los controles con la tecla MAYÚS presionada o arrastrar el puntero del mouse sobre los controles que desea seleccionar. Si selecciona múltiples controles, la hoja de propiedades mostrará sólo aquellas propiedades que tienen en común los controles seleccionados.
    
   - Una sección. Haga clic en el selector de sección de la sección que desea seleccionar.
    
   - El formulario o informe completo. Haga clic en el selector de formulario o en el selector de informe en la esquina superior izquierda del formulario o informe.

2. Muestre la hoja de propiedades haciendo clic con el botón secundario en el objeto o sección y luego eligiendo **Propiedades** en el menú contextual, o eligiendo **Propiedades** en la barra de herramientas.

3. Elija la propiedad para la que desea establecer el valor, y luego haga una de las siguientes cosas:
    
   - En el cuadro de la propiedad, escriba el valor o expresión apropiado.
    
   - Si el cuadro de la propiedad contiene una flecha, haga clic en la flecha y luego elija un valor de la lista.
    
   - Si aparece un botón **Generar** a la derecha del cuadro de la propiedad, haga clic en el mismo para mostrar un generador o para mostrar un cuadro de diálogo que le dé la opción de elegir generadores. Por ejemplo, puede usar el Generador de código, Generador de macros, o el Generador de consultas para establecer algunas propiedades.

## <a name="tips"></a>Sugerencias 

- Microsoft Access dispone de un cuadro **Zoom** para escribir y presentar expresiones u otros valores de propiedades largas. Para mostrar el cuadro **Zoom**, haga clic en un cuadro de propiedad en la hoja de propiedades. Luego presione MAYÚS+F2, o haga clic con el botón secundario y luego elija **Zoom** en el menú contextual.

- Puede establecer la propiedad **OrigenDelControl (ControlSource)** para algunos controles escribiendo el valor de la propiedad en el propio control.

- Puede cambiar los valores predeterminados de la propiedad para un tipo de control, de tal forma que los controles futuros que cree tengan estos nuevos valores predeterminados.

- Los valores de la propiedad de un control dependiente pueden no coincidir con los valores correspondientes en el campo de la tabla o consulta base del que es dependiente el control. Si los valores son distintos, los valores del formulario o del informe invalidan normalmente a los de la tabla o consulta. Para obtener más información sobre cómo se heredan las propiedades, vea Cómo se relacionan las propiedades de control con las propiedades de sus campos subyacentes.

