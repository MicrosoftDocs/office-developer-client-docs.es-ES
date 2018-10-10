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
# <a name="marshaloptions-property-ado"></a>MarshalOptions (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica qué registros se van a ordenar de nuevo en el servidor.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [MarshalOptionsEnum](marshaloptionsenum.md). El valor predeterminado es **adMarshalAll**.

## <a name="remarks"></a>Comentarios

Cuando se usa un objeto [Recordset](recordset-object-ado.md) de cliente, los registros modificados en el cliente se vuelven a escribir en el nivel intermedio o en el servidor web mediante una técnica denominada cálculo de referencias, que consiste en empaquetar y enviar parámetros de métodos de interfaz a través de los límites de subprocesos o procesos. Al establecer la propiedad **MarshalOptions**, se puede mejorar el rendimiento durante el cálculo de referencias de los datos remotos modificados para volver a actualizarse en el nivel intermedio o en el servidor web.

**Uso de servicio de datos remotos** Esta propiedad se utiliza sólo en un **conjunto de registros**de lado cliente.

