---
title: AbsolutePage (propiedad, ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280687"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="1afca-102">AbsolutePage (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="1afca-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="1afca-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1afca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1afca-104">Indica en qué página reside el registro actual.</span><span class="sxs-lookup"><span data-stu-id="1afca-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1afca-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="1afca-105">Settings and return values</span></span>

<span data-ttu-id="1afca-106">Establece o devuelve un valor de **tipo Long** comprendido entre 1 y el número de páginas del objeto [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)), o bien, devuelve uno de los valores de [PositionEnum](positionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="1afca-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1afca-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1afca-107">Remarks</span></span>

<span data-ttu-id="1afca-p101">Esta propiedad puede usarse para identificar el número de página donde está ubicado el registro actual. Usa la propiedad [PageSize](pagesize-property-ado.md) para dividir lógicamente el número total de conjuntos de filas del objeto **Recordset** en series de páginas, cada una con un número de registros equivalente a **PageSize** (salvo en el caso de la última página, que puede tener menos registros). El proveedor debe admitir la funcionalidad apropiada para que esta propiedad esté disponible.</span><span class="sxs-lookup"><span data-stu-id="1afca-p101">This property can be used to identify the page number on which the current record is located. It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records). The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="1afca-111">Al obtener o establecer la propiedad **AbsolutePage**, ADO usa la propiedad [AbsolutePosition](absoluteposition-property-ado.md) y la propiedad [PageSize](pagesize-property-ado.md) conjuntamente de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1afca-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="1afca-112">Para obtener el valor de **AbsolutePage**, ADO recupera primero el valor de **AbsolutePosition** y, a continuación, lo divide entre el valor de **PageSize**.</span><span class="sxs-lookup"><span data-stu-id="1afca-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="1afca-113">Para establecer el valor de **AbsolutePage**, ADO mueve **AbsolutePosition** de la siguiente forma: multiplica el valor de **PageSize** por el nuevo valor de **AbsolutePage** y, a continuación, le suma 1.</span><span class="sxs-lookup"><span data-stu-id="1afca-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="1afca-114">Como resultado, la posición actual del **objeto Recordset** después de establecer correctamente **AbsolutePage** es el primer registro de esa página.</span><span class="sxs-lookup"><span data-stu-id="1afca-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="1afca-p103">Al igual que la propiedad **AbsolutePosition**, **AbsolutePage** se basa en 1 y es igual a 1 cuando el registro actual es el primer registro del objeto **Recordset**. Establezca esta propiedad para desplazarse al primer registro de una página determinada. Obtenga el número total de páginas de la propiedad **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="1afca-p103">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

