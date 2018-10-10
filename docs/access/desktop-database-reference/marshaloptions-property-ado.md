---
title: MarshalOptions (propiedad, ADO)
TOCTitle: MarshalOptions Property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f290f2f4fb4820fb01d3a63aef7bcfbfa7c1f035
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485880"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="d6f1e-102">MarshalOptions (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="d6f1e-102">MarshalOptions Property (ADO)</span></span>


<span data-ttu-id="d6f1e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6f1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d6f1e-104">Indica qué registros se van a ordenar de nuevo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d6f1e-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d6f1e-105">Settings And Return Values</span></span>

<span data-ttu-id="d6f1e-p101">Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f1e-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d6f1e-108">Remarks</span></span>

<span data-ttu-id="d6f1e-p102">Cuando se usa un objeto [Recordset](recordset-object-ado.md) de cliente, los registros modificados en el cliente se vuelven a escribir en el nivel intermedio o en el servidor web mediante una técnica denominada cálculo de referencias, que consiste en empaquetar y enviar parámetros de métodos de interfaz a través de los límites de subprocesos o procesos. Al establecer la propiedad **MarshalOptions**, se puede mejorar el rendimiento durante el cálculo de referencias de los datos remotos modificados para volver a actualizarse en el nivel intermedio o en el servidor web.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-p102">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries. Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>

<span data-ttu-id="d6f1e-111">**Uso de servicio de datos remotos** Esta propiedad se utiliza sólo en un **conjunto de registros**de lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d6f1e-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

