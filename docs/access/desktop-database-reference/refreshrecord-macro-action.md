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
# <a name="refreshrecord-macro-action"></a><span data-ttu-id="c4ec0-102">ActualizarRegistro (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="c4ec0-102">RefreshRecord macro action</span></span>


<span data-ttu-id="c4ec0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4ec0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4ec0-104">Puede utilizar la acción **ActualizarRegistro** para actualizar el origen de registros subyacente para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en los registros del conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-104">You can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ec0-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4ec0-105">Remarks</span></span>

<span data-ttu-id="c4ec0-p101">La acción **ActualizarRegistro** muestra solo los cambios realizados en los registros del conjunto actual. Dado que la acción **ActualizarRegistro** realmente no vuelve a ejecutar la consulta en la base de datos, el conjunto actual no incluirá los registros que se hayan agregado ni excluirá los registros que se hayan eliminado desde la última vez se volvió a ejecutar la consulta en la base de datos. Tampoco excluirá los registros que ya no cumplan los criterios de la consulta o filtro. Para volver a ejecutar la consulta en la base de datos, utilice el método **[Requery](requery-macro-action.md)**. Si se vuelve a ejecutar la consulta del origen de registros de un formulario, el conjunto actual de registros reflejará con precisión todos los datos del origen de registros.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-p101">the **RefreshRecord** action shows only changes made to records in the current set. Because the **RefreshRecord** action does not actually requery the database, the current set will not include records that have been added or exclude records that have been deleted since the database was last requeried; Nor will it exclude records that no longer satisfy the criteria of the query or filter. To requery the database, use the **[Requery](requery-macro-action.md)** method. When the record source for a form is requeried, the current set of records will accurately reflect all data in the record source.</span></span>

<span data-ttu-id="c4ec0-110">El comportamiento de esta acción de macro depende de si se está llamando en una base de datos cliente o en una base de datos web.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-110">The behavior of this macro action depends on whether you are calling it in a client database or a web database.</span></span>

## <a name="client-database"></a><span data-ttu-id="c4ec0-111">Base de datos cliente</span><span class="sxs-lookup"><span data-stu-id="c4ec0-111">Client database</span></span>

<span data-ttu-id="c4ec0-p102">En una base de datos cliente, puede utilizar la acción **ActualizarRegistro** para actualizar el origen de registros subyacente para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en los datos del conjunto actual. Los cambios incluyen los realizados por el usuario actual o por otros usuarios en un entorno multiusuario. Es equivalente al método **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-p102">In a client database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the data in the current set. Changes include those made by the current user or by other users in a multiuser environment. It is equivalent to the **[Refresh](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)** method.</span></span>

<span data-ttu-id="c4ec0-115">La acción de macro **ActualizarRegistro** realiza lo siguiente en una base de datos cliente:</span><span class="sxs-lookup"><span data-stu-id="c4ec0-115">The **RefreshRecord** macro action does the following in a client database:</span></span>

1.  <span data-ttu-id="c4ec0-p103">Actualiza el origen de registros para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en las filas del conjunto actual. En tablas vinculadas ODBC, recupera los cambios realizados en los registros del conjunto actual desde el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-p103">Updates the record source for the active form or datasheet to reflect the changes made to rows in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="c4ec0-118">Actualiza el conjunto actual para reflejar los cambios.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-118">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="c4ec0-119">Si se ha eliminado una fila del origen de registros, se cambia para mostrar \#eliminada.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-119">If a row in the record source has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="c4ec0-120">Actualiza el activo o la hoja de información para mostrar los registros modificados y \#los registros eliminados en el conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-120">Refreshes the active or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="c4ec0-121">Vuelve a ejecutar la consulta en los subformularios y subinformes del formulario o la hoja de datos que esté activo.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-121">Requeries any subforms and subreports on the active form or datasheet.</span></span>

## <a name="web-database"></a><span data-ttu-id="c4ec0-122">Base de datos web</span><span class="sxs-lookup"><span data-stu-id="c4ec0-122">Web database</span></span>

<span data-ttu-id="c4ec0-p105">En una base de datos web, puede utilizar la acción **ActualizarRegistro** para actualizar el origen de registros subyacente para el formulario o la hoja de datos que esté activo con el fin de reflejar los cambios realizados en los registros del conjunto actual. Los cambios incluyen los realizados por el usuario actual u otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-p105">In a web database, you can use the **RefreshRecord** action to update the underlying record source for the active form or datasheet to reflect changes made to the records in the current set. Changes include those made by the current user or other users.</span></span>

<span data-ttu-id="c4ec0-125">La acción de macro **ActualizarRegistro** realiza lo siguiente en una base de datos web:</span><span class="sxs-lookup"><span data-stu-id="c4ec0-125">The **RefreshRecord** macro action does the following in a web database:</span></span>

1.  <span data-ttu-id="c4ec0-p106">Recupera del servidor los cambios realizados en las tablas base del conjunto actual. En tablas vinculadas ODBC, recupera los cambios realizados en los registros del conjunto actual desde el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-p106">Retrieves changes from the server for any base tables in the current set. For ODBC linked tables, retrieves changes to records in the current set from the data source.</span></span>

2.  <span data-ttu-id="c4ec0-128">Actualiza el conjunto actual para reflejar los cambios.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-128">Updates the current set to reflect the changes.</span></span> <span data-ttu-id="c4ec0-129">Si se ha eliminado una fila del conjunto actual, se cambia para mostrar \#eliminada.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-129">If a row in the current set has been deleted, it is changed to show \#Deleted.</span></span>

3.  <span data-ttu-id="c4ec0-130">Actualiza el formulario o la hoja de información activos para mostrar los registros modificados y \#los registros eliminados en el conjunto actual.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-130">Refreshes the active form or datasheet to display any changed records and any \#Deleted records, in the current set.</span></span>

4.  <span data-ttu-id="c4ec0-131">Vuelve a ejecutar la consulta en los subformularios y subinformes del formulario o la hoja de datos que esté activo.</span><span class="sxs-lookup"><span data-stu-id="c4ec0-131">Requeries any subforms and subreports on the active form or datasheet.</span></span>

