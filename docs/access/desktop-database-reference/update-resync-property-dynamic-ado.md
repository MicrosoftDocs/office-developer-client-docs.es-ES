---
title: Actualizar la propiedad dinámica Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f1443d1f2a4eccd8599256425a971bc63cd4d8b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918985"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="344a9-102">Actualizar la propiedad dinámica Resync (ADO)</span><span class="sxs-lookup"><span data-stu-id="344a9-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="344a9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="344a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="344a9-104">Especifica si el método [UpdateBatch](updatebatch-method-ado.md) es seguido por una operación implícita del método [Resync](resync-method-ado.md) y, si es así, el ámbito de esa operación.</span><span class="sxs-lookup"><span data-stu-id="344a9-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="344a9-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="344a9-105">Settings and return values</span></span>

<span data-ttu-id="344a9-106">Establece o devuelve uno o varios de los [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valores.</span><span class="sxs-lookup"><span data-stu-id="344a9-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="344a9-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="344a9-107">Remarks</span></span>

<span data-ttu-id="344a9-108">Los valores de ADCPROP\_UPDATERESYNC\_ENUM se puede combinar, excepto adResyncAll, que ya representa la combinación del resto de los valores.</span><span class="sxs-lookup"><span data-stu-id="344a9-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="344a9-109">La constante **adResyncConflicts** almacena los valores de resincronización como valores subyacentes, aunque no reemplaza los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="344a9-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="344a9-110">**Update Resync** es una propiedad dinámica que se anexa a la colección [Properties](recordset-object-ado.md) del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="344a9-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

