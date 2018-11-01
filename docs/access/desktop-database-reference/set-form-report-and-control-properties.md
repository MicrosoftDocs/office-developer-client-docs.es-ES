---
title: Establecer propiedades de formularios, informes y controles
TOCTitle: Set form, report, and control properties
description: Cada formulario, informe, sección y control tienen valores de propiedad que se pueden cambiar para alterar el aspecto o comportamiento de ese elemento determinado en Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2ffb02f78bbf9d9f4c5d5b07c1ee08e3f19453b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874611"
---
# <a name="set-form-report-and-control-properties"></a>Establecer propiedades de formularios, informes y controles

**Se aplica a**: Access 2013, Office 2013

Cada formulario, informe, sección y control tiene valores de propiedades que puede cambiar para alterar la apariencia o comportamiento de ese elemento determinado. Las propiedades se examinan y se cambian usando la hoja de propiedades, una macro, o Visual Basic.

## <a name="set-properties"></a>Establecer las propiedades

1. En la vista Diseño del formulario o vista Diseño del informe, seleccione el control, sección, formulario o informe para el que desea establecer la propiedad. Puede seleccionar:
    
   - Uno o varios controles. Para seleccionar varios controles, mantenga presionada la tecla MAYÚS y seleccione los controles o, arrastre el puntero del mouse sobre los controles que desea seleccionar. Si selecciona varios controles, la hoja de propiedades mostrará sólo aquellas propiedades que los controles seleccionados tienen en común.
    
   - Una sección. Elija el selector de sección de la sección que desea seleccionar.
    
   - El formulario o informe completo. Elija el selector de formulario o en el selector de informe en la esquina superior izquierda del formulario o informe.

2. Mostrar la hoja de propiedades por bien el objeto o sección y, a continuación, elija **Propiedades** en el menú contextual, o eligiendo **Propiedades** en la barra de herramientas.

3. Elija la propiedad para la que desea establecer el valor y, a continuación, realice una de las siguientes opciones:
    
   - En el cuadro de la propiedad, escriba el valor o expresión apropiado.
    
   - Si el cuadro de la propiedad contiene una flecha, elija la flecha y, a continuación, elija un valor en la lista.
    
   - Si aparece un botón **Generar** a la derecha del cuadro de la propiedad, elija para mostrar un generador o para mostrar un cuadro de diálogo que le una opción de elegir generadores. Por ejemplo, puede usar el Generador de código, Generador de macros, o el Generador de consultas para establecer algunas propiedades.

## <a name="tips"></a>Sugerencias 

- Microsoft Access dispone de un cuadro **Zoom** para escribir y presentar expresiones u otros valores de propiedades largas. Para mostrar el cuadro **Zoom** , elija un cuadro de propiedad en la hoja de propiedades. Presione MAYÚS + F2 o con el botón secundario y, a continuación, elija **Zoom** en el menú contextual.

- Puede establecer la propiedad **OrigenDelControl (ControlSource)** para algunos controles escribiendo el valor de la propiedad en el propio control.

- Puede cambiar los valores predeterminados de la propiedad para un tipo de control, de tal forma que los controles futuros que cree tengan estos nuevos valores predeterminados.

- Los valores de la propiedad de un control dependiente pueden no coincidir con los valores correspondientes en el campo de la tabla o consulta base del que es dependiente el control. Si los valores son distintos, los valores del formulario o del informe invalidan normalmente a los de la tabla o consulta.

