---
title: FetchProgress (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72a860ecd52e0481b55423f88e537eab3c8de2ae
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485069"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress (ADO)


**Se aplica a**: Access 2013 | Office 2013


Al evento **FetchProgress** se le llama periódicamente durante una operación asincrónica prolongada para informar de cuántas filas se han recuperado e insertado actualmente en el objeto [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Sintaxis

De*progreso*, *MaxProgress*, FetchProgress *adStatus*, *pRecordset*

## <a name="parameters"></a>Parámetros

  - *Progress*

  - Valor **Long** que indica el número de registros que han sido recuperados actualmente por la operación de búsqueda.

  - *MaxProgress*

  - Valor **Long** que indica el número máximo de registros que se espera recuperar.

  - *valor de adStatus*

  - Valor de estado [EventStatusEnum](eventstatusenum.md).

  - *Connection*

  - Objeto **Recordset** para el que se están recuperando los registros.

## <a name="remarks"></a>Comentarios

Cuando utilice **FetchProgress** con un **Recordset**secundario, tenga en cuenta que los valores de parámetro *Progress* y *MaxProgress* se derivan del conjunto de filas subyacente [Del servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md) . Los valores devueltos representan el número total de registros en el conjunto de filas subyacente, no solo el número de registros en el capítulo actual.


> [!NOTE]
> <P>[!NOTA] Para utilizar <STRONG>FetchProgress</STRONG> con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.</P>


