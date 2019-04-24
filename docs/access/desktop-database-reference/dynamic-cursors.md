---
title: Cursores dinámicos (referencia de base de datos de escritorio de Access)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293640"
---
# <a name="dynamic-cursors"></a>Cursores dinámicos


**Se aplica a:** Access 2013, Office 2013

Los cursores dinámicos detectan todos los cambios realizados en las filas del conjunto de resultados, independientemente de que los cambios se produzcan desde dentro del cursor o los realicen otros usuarios ajenos al cursor. Todas las instrucciones para inserción, actualización y eliminación realizadas por todos los usuarios se pueden ver a través del cursor. El cursor dinámico puede detectar cualquier cambio realizado en las filas, en el orden y en los valores del conjunto de resultados después de abrirse el cursor. Las actualizaciones realizadas fuera del cursor no son visibles hasta que se confirman (a menos que el nivel de aislamiento de la transacción del cursor esté establecido en "no guardados").

Por ejemplo, suponga que un cursor dinámico recupera dos filas y otra aplicación y que, a continuación, actualiza una de esas filas y elimina la otra. Si, luego, el cursor dinámico recupera esas filas, no encontrará la fila eliminada pero mostrará los valores nuevos de la fila actualizada.

El cursor dinámico es una buena elección si una aplicación debe detectar todas las actualizaciones simultáneas realizadas por otros usuarios. Utilice el valor **adOpenDynamic** de **CursorTypeEnum** para indicar que desea utilizar un cursor dinámico en ADO.

[Cursores de sólo avance](forward-only-cursors.md) | [Cursores estáticos](static-cursors.md) | [Cursores con conjunto de claves](keyset-cursors.md)

