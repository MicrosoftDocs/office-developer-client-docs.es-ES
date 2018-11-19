---
title: SubmitChanges (método, RDS)
TOCTitle: SubmitChanges method (RDS)
ms:assetid: ecaea12d-7e1a-095d-17e7-d631ef230b90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250201(v=office.15)
ms:contentKeyID: 48548521
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b5c18aa12519e9206702eb2a152e6f0d084edc9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026347"
---
# <a name="submitchanges-method-rds"></a>SubmitChanges (método, RDS)

**Se aplica a**: Access 2013, Office 2013

Envía los cambios pendientes del objeto [Recordset](recordset-object-ado.md) almacenado en caché local y actualizable al origen de datos especificado en la propiedad [Connect](connect-property-rds.md) o la propiedad [URL](url-property-rds.md).

## <a name="syntax"></a>Sintaxis

*DataControl*. SubmitChanges

*DataFactory*. SubmitChanges*conexión*, *conjunto de registros*

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

**SubmitChanges** puede utilizarse únicamente con el objeto **RDSServer.DataFactory** *predeterminado* . Los objetos de negocio personalizados no pueden utilizar este método.

Si se ha definido la propiedad **URL**, **SubmitChanges** enviará los cambios a la ubicación especificada por la dirección URL.

