---
title: MarshalOptions (propiedad, ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704598"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="8ccfc-102">MarshalOptions (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="8ccfc-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="8ccfc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ccfc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ccfc-104">Indica qué registros se van a ordenar de nuevo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8ccfc-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8ccfc-105">Settings And Return Values</span></span>

<span data-ttu-id="8ccfc-p101">Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ccfc-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ccfc-108">Remarks</span></span>

<span data-ttu-id="8ccfc-109">Cuando se usa un [conjunto de registros](recordset-object-ado.md)de lado cliente, los registros que se han modificado en el cliente se vuelven a escribir el nivel intermedio o el servidor web a través de una técnica denominada el cálculo de referencias, el proceso de empaquetar y enviar parámetros de método de interfaz a través de subproceso o límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="8ccfc-110">Al establecer la propiedad **MarshalOptions** puede mejorar el rendimiento cuando datos remotos modificados se calculan las referencias para volver a actualizarse el nivel intermedio o el servidor web.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="8ccfc-111">**Uso de servicio de datos remotos** Esta propiedad se utiliza sólo en un **conjunto de registros**de lado cliente.</span><span class="sxs-lookup"><span data-stu-id="8ccfc-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

