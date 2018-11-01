---
title: dinámica Update Resync (propiedad, ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57b7fd5dadf6b4da3239cc208744691ce22e62f1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880477"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="c8425-102">dinámica Update Resync (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="c8425-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="c8425-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8425-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8425-104">Especifica si el método [UpdateBatch](updatebatch-method-ado.md) es seguido por una operación implícita del método [Resync](resync-method-ado.md) y, si es así, el ámbito de esa operación.</span><span class="sxs-lookup"><span data-stu-id="c8425-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c8425-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="c8425-105">Settings and return values</span></span>

<span data-ttu-id="c8425-106">Establece o devuelve uno o varios de los [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valores.</span><span class="sxs-lookup"><span data-stu-id="c8425-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8425-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8425-107">Remarks</span></span>

<span data-ttu-id="c8425-108">Los valores de ADCPROP\_UPDATERESYNC\_ENUM se puede combinar, excepto adResyncAll, que ya representa la combinación del resto de los valores.</span><span class="sxs-lookup"><span data-stu-id="c8425-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="c8425-109">La constante **adResyncConflicts** almacena los valores de resincronización como valores subyacentes, aunque no reemplaza los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="c8425-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="c8425-110">**Update Resync** es una propiedad dinámica que se anexa a la colección [Properties](recordset-object-ado.md) del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="c8425-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

