---
title: SubmitChanges (método, RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92634f2c0d95fbe9022934d22340f768b5614a58
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923374"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges (método, RDS)


**Se aplica a**: Access 2013, Office 2013

Envía los cambios pendientes del objeto [Recordset](recordset-object-ado.md) almacenado en caché local y actualizable al origen de datos especificado en la propiedad [Connect](connect-property-rds.md) o la propiedad [URL](url-property-rds.md).

## <a name="syntax"></a>Sintaxis

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges*conexión*, *conjunto de registros*

## <a name="parameters"></a>Parámetros

  - *DataControl*

  - Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *DataFactory*

  - Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).

  - *Connection*

  - Valor de tipo **String** que representa la conexión creada con la propiedad **Connect** del objeto **RDS.DataControl**.

  - *Recordset*

  - Variable de objeto que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) deben establecerse primero para que se pueda utilizar el método **SubmitChanges** con el objeto **RDS.DataControl**.

Si se llama al método [CancelUpdate](cancelupdate-method-rds.md) después de llamar a **SubmitChanges** del mismo objeto **Recordset**, la llamada a **CancelUpdate** generará un error porque ya se han confirmado los cambios.

Sólo se envían los registros cambiados para su modificación. Los cambios se realizan todos correctamente, o bien, todos juntos generan un error.

**SubmitChanges** puede utilizarse únicamente con el objeto **RDSServer.DataFactory** *predeterminado* . Los objetos de negocio personalizados no pueden utilizar este método.

Si se ha definido la propiedad **URL**, **SubmitChanges** enviará los cambios a la ubicación especificada por la dirección URL.

