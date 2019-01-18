---
title: Control de errores en Visual C++
TOCTitle: Handling errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d0e76dc3cc9634a1531a34058bf7a1baf636c94c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709477"
---
# <a name="handling-errors-in-visual-c"></a>Control de errores en Visual C++


**Se aplica a**: Access 2013, Office 2013

En COM, la mayoría de las operaciones devolverá un código de retorno HRESULT que indica si una función se completó correctamente. El \#directiva de importación genera código contenedor alrededor de cada método "sin procesar" o la propiedad y comprueba el HRESULT devuelto. Si el HRESULT indica error, el código de contenedor genera un error COM llamando a \_com\_problema\_errorex() con el HRESULT devolver código como un argumento. Objetos de error COM se pueden capturar en un bloque **try-catch** . (Para una mayor eficacia, detecte una referencia a un \_com\_objeto error.)

Recuerde que se trata de errores de ADO: son el resultado de los errores de operaciones de ADO. Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.

El \#directiva de importación sólo crea rutinas de tratamiento de errores para métodos y propiedades declarados en la DLL de ADO. No obstante, puede sacar partido de este mismo mecanismo de control de errores escribiendo su propia macro o función en línea de comprobación de errores. Vea ejemplos en el tema Extensiones de Visual C++.

