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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292030"
---
# <a name="handling-errors-in-visual-c"></a>Control de errores en Visual C++


**Se aplica a:** Access 2013, Office 2013

In COM, most operations return an HRESULT return code that indicates whether a function completed successfully. La directiva de importación genera código contenedor alrededor de cada propiedad o \# método "sin procesar" y comprueba el HRESULT devuelto. Si el HRESULT indica un error, el código contenedor genera un error COM llamando a \_ com issue errorex() con el código de retorno \_ \_ HRESULT como argumento. Los objetos de error COM se pueden capturar en un **bloque try-catch.** (Por razones de eficiencia, captura una referencia a un objeto \_ \_ de error com).

Recuerde que se trata de errores de ADO: son el resultado de los errores de operaciones de ADO. Los errores devueltos por el proveedor subyacente aparecen como objetos **Error** de la colección **Errors** del objeto **Connection**.

La directiva de importación solo crea rutinas de control de errores \# para métodos y propiedades declarados en el archivo .dll de ADO. No obstante, puede sacar partido de este mismo mecanismo de control de errores escribiendo su propia macro o función en línea de comprobación de errores. Vea ejemplos en el tema Extensiones de Visual C++.

