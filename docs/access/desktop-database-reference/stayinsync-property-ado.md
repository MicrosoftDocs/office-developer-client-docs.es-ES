---
title: Propiedad StayInSync (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308494"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="499ea-102">Propiedad StayInSync (ADO)</span><span class="sxs-lookup"><span data-stu-id="499ea-102">StayInSync property (ADO)</span></span>


<span data-ttu-id="499ea-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="499ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="499ea-104">En un objeto [Recordset](recordset-object-ado.md) jerárquico, indica si la referencia a los registros secundarios subyacentes (es decir, el *capítulo*) cambia cuando la posición de la fila superior en la jerarquía (elemento principal) cambia.</span><span class="sxs-lookup"><span data-stu-id="499ea-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="499ea-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="499ea-105">Settings and return values</span></span>

<span data-ttu-id="499ea-p101">Establece o devuelve un valor de tipo **Boolean**. El valor predeterminado es **True**. Si es **True**, el capítulo se actualizará si el objeto **Recordset** primario cambia la posición de la fila; si es **False**, seguirá haciendo referencia a los datos del capítulo anterior, aun cuando el objeto **Recordset** primario haya cambiado la posición de la fila.</span><span class="sxs-lookup"><span data-stu-id="499ea-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="499ea-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="499ea-109">Remarks</span></span>

<span data-ttu-id="499ea-p102">Esta propiedad se aplica a objetos Recordset jerárquicos, como los admitidos por el [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), y debe establecerse en el objeto **Recordset** primario antes de que el objeto **Recordset** secundario sea recuperado. Esta propiedad simplifica el desplazamiento por los conjuntos de registros jerárquicos.</span><span class="sxs-lookup"><span data-stu-id="499ea-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

