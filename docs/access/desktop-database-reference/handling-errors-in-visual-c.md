---
title: Tratar errores en Visual C++
TOCTitle: Handling Errors in Visual C++
ms:assetid: 75e15699-0c84-1dca-654e-f9ac465c2a30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249483(v=office.15)
ms:contentKeyID: 48545684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8feeb97e049d245da91371fdb5225a644d0e415
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484240"
---
# <a name="handling-errors-in-visual-c"></a>Tratar errores en Visual C++


**Se aplica a**: Access 2013 | Office 2013

En COM, la mayoría de las operaciones devolverá un código de retorno HRESULT que indica si una función se completó correctamente. El \#directiva de importación genera código contenedor alrededor de cada método "sin procesar" o la propiedad y comprueba el HRESULT devuelto. Si el HRESULT indica error, el código de contenedor genera un error COM llamando a \_com\_problema\_errorex() con el HRESULT devolver código como un argumento. Objetos de error COM se pueden capturar en un bloque **try-catch** . (Para una mayor eficacia, detecte una referencia a un \_com\_objeto error.)

Recuerde que se trata de errores de ADO: son el resultado de los errores de operaciones de ADO. Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.

El \#directiva de importación sólo crea rutinas de tratamiento de errores para métodos y propiedades declarados en la DLL de ADO. No obstante, puede sacar partido de este mismo mecanismo de control de errores escribiendo su propia macro o función en línea de comprobación de errores. Vea ejemplos en el tema Extensiones de Visual C++.

