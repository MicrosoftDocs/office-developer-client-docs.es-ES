---
title: Desconectar y volver a conectar el objeto Recordset
TOCTitle: Disconnecting and Reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90435606bb0b3059f5769c12fe7cf3cac0c8f9f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486640"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a>Desconectar y volver a conectar el objeto Recordset


**Se aplica a**: Access 2013 | Office 2013

## <a name="disconnecting-and-reconnecting-the-recordset"></a>Desconectar y volver a conectar el objeto Recordset

Una de las características más eficaces de ADO es la posibilidad de abrir un **conjunto de registros** de cliente desde un origen de datos y, a continuación, *desconectar* el **conjunto de registros** del origen de datos. Una vez desconectado el **conjunto de registros**, se puede cerrar la conexión con el origen de datos para liberar así los recursos del servidor que se utilizan para mantenerla. Puede continuar viendo y modificando los datos del **conjunto de registros** mientras está desconectado y, más tarde, volver a conectarse al origen de datos para enviar sus actualizaciones en modo de proceso por lotes.

Para desconectar un **conjunto de registros**, ábralo con una ubicación de cursor de **adUseClient** y, a continuación, establezca la propiedad **ActiveConnection** en *Nothing* (los usuarios de C++ deben establecer **ActiveConnection** en NULL para desconectar).

Más adelante en este capítulo, se utilizará un **conjunto de registros** desconectado cuando se hable de la persistencia de **conjuntos de registros** para afrontar un escenario en el que se necesita tener los datos de un **conjunto de registros** disponibles para una aplicación mientras el equipo cliente no está conectado a una red.

