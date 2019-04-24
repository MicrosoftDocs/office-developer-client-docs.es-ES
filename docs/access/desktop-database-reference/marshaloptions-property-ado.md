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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289773"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="20672-102">MarshalOptions (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="20672-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="20672-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20672-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20672-104">Indica qué registros se van a ordenar de nuevo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="20672-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="20672-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="20672-105">Settings And Return Values</span></span>

<span data-ttu-id="20672-p101">Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="20672-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20672-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20672-108">Remarks</span></span>

<span data-ttu-id="20672-109">Cuando se usa un [objeto Recordset](recordset-object-ado.md)de cliente, los registros modificados en el cliente se vuelven a escribir en el nivel intermedio o el servidor Web mediante una técnica denominada cálculo de referencias, el proceso de empaquetar y enviar parámetros de métodos de interfaz a través de subprocesos o límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="20672-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="20672-110">El establecimiento de la propiedad **MarshalOptions** puede mejorar el rendimiento cuando se calculan las referencias de los datos remotos modificados para volver a actualizarse en el nivel intermedio o el servidor Web.</span><span class="sxs-lookup"><span data-stu-id="20672-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="20672-111">**Uso del servicio de datos remotos** Esta propiedad se usa únicamente en un **conjunto de registros**del cliente.</span><span class="sxs-lookup"><span data-stu-id="20672-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

