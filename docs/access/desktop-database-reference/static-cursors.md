---
title: Cursores estáticos (referencia de escritorio de la base de datos de Access)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2eb019a6fc960d58771ff5ab0de7dca547c55f1c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699523"
---
# <a name="static-cursors"></a>Cursores estáticos


**Se aplica a**: Access 2013, Office 2013

El cursor estático siempre muestra el conjunto de resultados tal como era cuando el cursor se abrió por primera vez. Según la implementación, los cursores estáticos pueden ser de sólo lectura o de lectura y escritura, y proporcionar desplazamiento hacia adelante y hacia atrás. El cursor estático normalmente no detecta los cambios realizados en la pertenencia, en el orden ni en los valores del conjunto de resultados tras abrir el cursor. Los cursores estáticos pueden detectar sus propias actualizaciones, eliminaciones e inserciones, aunque no se requiere que lo hagan.

Los cursores estáticos no detectan nunca las actualizaciones, eliminaciones ni inserciones del resto de las aplicaciones. Por ejemplo, suponga que un cursor estático recupera una fila y otra aplicación la actualiza. Si la aplicación vuelve a obtener la fila desde el cursor estático, los valores que ve no reflejan los cambios realizados por la otra aplicación. Se admiten todos los tipos de desplazamiento, pero los proveedores pueden o no admitir marcadores.

Si la aplicación requiere desplazamientos y no necesita detectar cambios en los datos, el cursor estático es la mejor opción. Utilice **adOpenStatic** **CursorTypeEnum** para indicar que desea utilizar un cursor estático en ADO.

