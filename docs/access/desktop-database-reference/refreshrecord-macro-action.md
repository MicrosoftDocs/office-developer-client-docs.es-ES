---
title: ActualizarRegistro (acción de macro)
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307087"
---
# <a name="refreshrecord-macro-action"></a>ActualizarRegistro (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Puede utilizar la acción **ActualizarRegistro** para actualizar el origen de registros subyacente para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en los registros del conjunto actual.

## <a name="remarks"></a>Comentarios

La acción **ActualizarRegistro** muestra solo los cambios realizados en los registros del conjunto actual. Dado que la acción **ActualizarRegistro** realmente no vuelve a ejecutar la consulta en la base de datos, el conjunto actual no incluirá los registros que se hayan agregado ni excluirá los registros que se hayan eliminado desde la última vez se volvió a ejecutar la consulta en la base de datos. Tampoco excluirá los registros que ya no cumplan los criterios de la consulta o filtro. Para volver a ejecutar la consulta en la base de datos, utilice el método **[Requery](requery-macro-action.md)**. Si se vuelve a ejecutar la consulta del origen de registros de un formulario, el conjunto actual de registros reflejará con precisión todos los datos del origen de registros.

El comportamiento de esta acción de macro depende de si se está llamando en una base de datos cliente o en una base de datos web.

## <a name="client-database"></a>Base de datos cliente

En una base de datos cliente, puede utilizar la acción **ActualizarRegistro** para actualizar el origen de registros subyacente para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en los datos del conjunto actual. Los cambios incluyen los realizados por el usuario actual o por otros usuarios en un entorno multiusuario. Es equivalente al método **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**.

La acción de macro **ActualizarRegistro** realiza lo siguiente en una base de datos cliente:

1.  Actualiza el origen de registros para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en las filas del conjunto actual. En tablas vinculadas ODBC, recupera los cambios realizados en los registros del conjunto actual desde el origen de datos.

2.  Actualiza el conjunto actual para reflejar los cambios. Si se ha eliminado una fila en el origen del registro, se cambia para mostrar \# Deleted.

3.  Actualiza la hoja de datos o activa para mostrar los registros modificados y los \# registros eliminados en el conjunto actual.

4.  Vuelve a ejecutar la consulta en los subformularios y subinformes del formulario o la hoja de datos que esté activo.

## <a name="web-database"></a>Base de datos web

En una base de datos web, puede utilizar la acción **ActualizarRegistro** para actualizar el origen de registros subyacente para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en los registros del conjunto actual. Los cambios incluyen los realizados por el usuario actual u otros usuarios.

La acción de macro **ActualizarRegistro** realiza lo siguiente en una base de datos web:

1.  Recupera del servidor los cambios realizados en las tablas base del conjunto actual. En tablas vinculadas ODBC, recupera los cambios realizados en los registros del conjunto actual desde el origen de datos.

2.  Actualiza el conjunto actual para reflejar los cambios. Si se ha eliminado una fila del conjunto actual, se cambia para mostrar \# Eliminado.

3.  Actualiza el formulario activo o la hoja de datos para mostrar los registros modificados y los \# registros eliminados en el conjunto actual.

4.  Vuelve a ejecutar la consulta en los subformularios y subinformes del formulario o la hoja de datos que esté activo.

