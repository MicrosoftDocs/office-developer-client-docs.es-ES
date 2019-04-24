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
# <a name="marshaloptions-property-ado"></a>MarshalOptions (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica qué registros se van a ordenar de nuevo en el servidor.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.

## <a name="remarks"></a>Comentarios

Cuando se usa un [objeto Recordset](recordset-object-ado.md)de cliente, los registros modificados en el cliente se vuelven a escribir en el nivel intermedio o el servidor Web mediante una técnica denominada cálculo de referencias, el proceso de empaquetar y enviar parámetros de métodos de interfaz a través de subprocesos o límites del proceso. El establecimiento de la propiedad **MarshalOptions** puede mejorar el rendimiento cuando se calculan las referencias de los datos remotos modificados para volver a actualizarse en el nivel intermedio o el servidor Web.

**Uso del servicio de datos remotos** Esta propiedad se usa únicamente en un **conjunto de registros**del cliente.

