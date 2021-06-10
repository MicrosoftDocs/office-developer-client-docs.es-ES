---
title: Método SubmitChanges (RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ea7f3e27a75b4483cb8cf46e27d4492f831cff33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314402"
---
# <a name="submitchanges-method-rds"></a>Método SubmitChanges (RDS)

**Se aplica a:** Access 2013, Office 2013

Envía los cambios pendientes del objeto [Recordset](recordset-object-ado.md) almacenado en caché local y actualizable al origen de datos especificado en la propiedad [Connect](connect-property-rds.md) o la propiedad [URL](url-property-rds.md).

## <a name="syntax"></a>Sintaxis

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges *Connection*, *Recordset*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*DataFactory* |Variable de objeto que representa un objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connection* |Valor de tipo **String** que representa la conexión creada con la propiedad **Connect** del objeto **RDS.DataControl**.|
|*Recordset* |Variable de objeto que representa un objeto **Recordset**.|

## <a name="remarks"></a>Comentarios

Las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) deben establecerse primero para que se pueda utilizar el método **SubmitChanges** con el objeto **RDS.DataControl**.

Si se llama al método [CancelUpdate](cancelupdate-method-rds.md) después de llamar a **SubmitChanges** del mismo objeto **Recordset**, la llamada a **CancelUpdate** generará un error porque ya se han confirmado los cambios.

Sólo se envían los registros cambiados para su modificación. Los cambios se realizan todos correctamente, o bien, todos juntos generan un error.

Solo puede usar **SubmitChanges** con el *objeto* **RDSServer.DataFactory** predeterminado. Los objetos de negocio personalizados no pueden utilizar este método.

Si se ha definido la propiedad **URL**, **SubmitChanges** enviará los cambios a la ubicación especificada por la dirección URL.

