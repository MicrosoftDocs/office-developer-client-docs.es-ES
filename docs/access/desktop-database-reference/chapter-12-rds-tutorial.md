---
title: 'Capítulo 12: Tutorial de RDS'
TOCTitle: 'Chapter 12: RDS Tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a482da49bb78a74cc68f589c928ffe13dd4a54ad
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486198"
---
# <a name="chapter-12-rds-tutorial"></a>Capítulo 12: Tutorial de RDS


**Se aplica a**: Access 2013 | Office 2013

Este tutorial muestra el uso del modelo de programación RDS para consultar y actualizar un origen de datos. Primero, describe los pasos necesarios para realizar esta tarea. Después, el tutorial se repite en Microsoft® Visual Basic Scripting Edition y en Microsoft® Visual J++®, con la utilización de ADO para Windows Foundation Classes (ADO/WFC).

Este tutorial se codifica en diferentes lenguajes por dos motivos:

  - La documentación para RDS supone que el lector codifica en Visual Basic. Esto hace que la documentación sea más apropiada para programadores de Visual Basic, pero menos útil para los que utilizan otros lenguajes.

  - Si no está seguro de una determinada función de RDS y conoce algo de otro lenguaje, podría resolver sus dudas buscando la misma característica expresada en el otro lenguaje.

## <a name="how-the-tutorial-is-presented"></a>Cómo se presenta el tutorial

Este tutorial se basa en el modelo de programación RDS. Analiza individualmente cada paso del modelo de programación. Además, ilustra cada paso con un fragmento de código de Visual Basic.

El ejemplo de código se repite en otros lenguajes con una mínima descripción. Cada paso de un tutorial de un lenguaje de programación dado está marcado con el paso correspondiente del tutorial descriptivo y del modelo de programación. Utilice el número del paso como referencia a la explicación del tutorial descriptivo.

El modelo de programación RDS se especifica a continuación. Úselo como una guía mientras avanza en el tutorial.

## <a name="rds-programming-model-with-objects"></a>Modelo de programación de RDS con objetos

  - Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente.

  - Llame al programa de servidor. Pásele los parámetros que identifican el origen de datos y el comando que se desea emitir.

  - Normalmente, el programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos utilizando ADO. Opcionalmente, el objeto **Recordset** se procesa en el servidor.

  - El programa de servidor devuelve el objeto **Recordset** final a la aplicación cliente.

  - En el cliente, el objeto **Recordset** se coloca opcionalmente en un formulario que se puede usar fácilmente mediante controles visuales.

  - Los cambios realizados en el objeto **Recordset** se envían al servidor y se usan para actualizar el origen de datos.

