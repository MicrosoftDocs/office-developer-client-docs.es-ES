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
# <a name="marshaloptions-property-ado"></a>MarshalOptions (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica qué registros se van a ordenar de nuevo en el servidor.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.

## <a name="remarks"></a>Comentarios

Cuando se usa un [conjunto de registros](recordset-object-ado.md)de lado cliente, los registros que se han modificado en el cliente se vuelven a escribir el nivel intermedio o el servidor web a través de una técnica denominada el cálculo de referencias, el proceso de empaquetar y enviar parámetros de método de interfaz a través de subproceso o límites del proceso. Al establecer la propiedad **MarshalOptions** puede mejorar el rendimiento cuando datos remotos modificados se calculan las referencias para volver a actualizarse el nivel intermedio o el servidor web.

**Uso de servicio de datos remotos** Esta propiedad se utiliza sólo en un **conjunto de registros**de lado cliente.

