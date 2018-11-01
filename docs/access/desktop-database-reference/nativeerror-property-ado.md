---
title: NativeError (propiedad, ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d572e7629deca0c7732bafbdfdb0c600ce34a35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880183"
---
# <a name="nativeerror-property-ado"></a>NativeError (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el código de error específico de un proveedor para un objeto [Error](error-object-ado.md) dado.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que indica el código del error.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **NativeError** para recuperar información de error específica de base de datos de un objeto **Error** concreto. Por ejemplo, al utilizar el Proveedor de Microsoft OLE DB para ODBC con una base de datos de Microsoft SQL Server, los códigos de error nativos que se originan en SQL Server pasan a través de ODBC y el Proveedor ODBC a la propiedad **NativeError** de ADO.

