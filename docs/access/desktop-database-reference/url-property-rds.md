---
title: Propiedad URL (referencia de base de datos de escritorio de Access de RDS)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aafc8cc10410cafed21e38ad7fec269c391c1fa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313401"
---
# <a name="url-property-rds"></a>URL (propiedad, RDS)

**Se aplica a:** Access 2013, Office 2013

Indica una cadena que contiene una dirección URL relativa o absoluta.

Puede establecer la propiedad **URL** durante el diseño en las etiquetas OBJECT del objeto [DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.

## <a name="syntax"></a>Sintaxis

Tiempo de diseño \<: param name = "URL" Value = "Server"\>

Tiempo de ejecución: DataControl. URL = "Server"

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Server* |Un valor de tipo **String** que contiene una dirección URL válida.|
|*DataControl* |Una variable de objeto que representa un objeto **DataControl**.|

## <a name="remarks"></a>Comentarios

Normalmente, la dirección URL identifica a un archivo de páginas Active Server (.asp) que puede producir y devolver un objeto [Recordset](recordset-object-ado.md). Por lo tanto, el usuario puede obtener un objeto **Recordset** sin necesidad de llamar al objeto [DataFactory](datafactory-object-rdsserver.md) del servidor ni programar un objeto de negocio personalizado.

Si la propiedad **URL** se ha establecido, [SubmitChanges](submitchanges-method-rds.md) enviará los cambios a la ubicación especificada por la dirección URL.

