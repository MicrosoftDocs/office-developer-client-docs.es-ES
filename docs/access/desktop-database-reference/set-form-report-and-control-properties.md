---
title: Establecer propiedades de formularios, informes y controles
TOCTitle: Set form, report, and control properties
description: Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado en Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308739"
---
# <a name="set-form-report-and-control-properties"></a>Establecer propiedades de formularios, informes y controles

**Se aplica a:** Access 2013, Office 2013

Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado. Las propiedades se examinan y se cambian usando la hoja de propiedades, una macro, o Visual Basic.

## <a name="set-properties"></a>Establecer propiedades

1. En la vista Diseño del formulario o vista Diseño del informe, seleccione el control, sección, formulario o informe para el que desea establecer la propiedad. Puede seleccionar:
    
   - Uno o más controles. Para seleccionar controles múltiples, se puede hacer clic en los controles con la tecla MAYÚS presionada o arrastrar el puntero del ratón sobre los controles que desea seleccionar. If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.
    
   - Una sección. Haga clic en el selector de sección de la sección que quiere seleccionar.
    
   - Todo el formulario o informe. Haga clic en el selector de formulario o en el selector de informe en la esquina superior izquierda del formulario o informe.

2. Muestre la hoja de propiedades haciendo clic con el botón secundario en el objeto o sección y luego eligiendo **Propiedades** en el menú contextual, o eligiendo **Propiedades** en la barra de herramientas.

3. Elija la propiedad para la que desea establecer el valor, y luego haga una de las siguientes cosas:
    
   - En el cuadro de propiedades, escriba el valor o expresión apropiados.
    
   - Si el cuadro de la propiedad contiene una flecha, haga clic en la flecha y luego elija un valor de la lista.
    
   - Si aparece un botón **Generar** a la derecha del cuadro de la propiedad, haga clic en el mismo para mostrar un generador o para mostrar un cuadro de diálogo que le dé la opción de elegir generadores. Por ejemplo, puede usar el Generador de código, Generador de macros o Generador de consultas para establecer algunas propiedades.

## <a name="tips"></a>Sugerencias

- Microsoft Access proporciona un cuadro de **Zoom** para escribir y ver expresiones u otros valores de propiedades largos. Para mostrar el cuadro **Zoom**, haga clic en un cuadro de propiedad en la hoja de propiedades. Presione MAYÚS+F2, o haga clic con el botón secundario y luego elija **Zoom** en el menú contextual.

- Puede establecer la propiedad **OrigenDelControl (ControlSource)** para algunos controles escribiendo el valor de la propiedad en el propio control.

- Puede cambiar los valores predeterminados de la propiedad para un tipo de control, de tal forma que los controles futuros que cree tengan estos nuevos valores predeterminados.

- Los valores de la propiedad de un control dependiente pueden no coincidir con los valores correspondientes en el campo de la tabla o consulta base del que es dependiente el control. Si los valores son distintos, los valores del formulario o del informe invalidan normalmente a los de la tabla o consulta.

