---
title: Dirección URL (propiedad, RDS - referencia de escritorio de la base de datos de Access)
TOCTitle: URL Property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8d1e524df8f1921f712f9dce174ab90ebd57325
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483304"
---
# <a name="url-property-rds"></a>URL (propiedad, RDS)


**Se aplica a**: Access 2013 | Office 2013



Indica una cadena que contiene una dirección URL relativa o absoluta.

Puede establecer la propiedad **URL** durante el diseño en las etiquetas OBJECT del objeto [DataControl](datacontrol-object-rds.md) o en tiempo de ejecución en el código de scripting.

## <a name="syntax"></a>Sintaxis

Tiempo de diseño: \<PARAM NAME = "URL" VALUE = "Servidor"\>

Tiempo de ejecución: DataControl.URL="Server"

## <a name="parameters"></a>Parámetros

  - *Server*

  - Un valor de tipo **String** que contiene una dirección URL válida.

  - *DataControl*

  - Una variable de objeto que representa un objeto **DataControl**.

## <a name="remarks"></a>Comentarios

Normalmente, la dirección URL identifica a un archivo de páginas Active Server (.asp) que puede producir y devolver un objeto [Recordset](recordset-object-ado.md). Por lo tanto, el usuario puede obtener un objeto **Recordset** sin necesidad de llamar al objeto [DataFactory](datafactory-object-rdsserver.md) del servidor ni programar un objeto de negocio personalizado.

Si la propiedad **URL** se ha establecido, [SubmitChanges](submitchanges-method-rds.md) enviará los cambios a la ubicación especificada por la dirección URL.

