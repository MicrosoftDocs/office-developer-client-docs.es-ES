---
title: Propiedad QueryDef.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716694"
---
# <a name="querydefstillexecuting-property-dao"></a>Propiedad QueryDef.StillExecuting (DAO)


**Se aplica a**: Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . StillExecuting

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

Use la propiedad **StillExecuting** para determinar si el método asincrónico **[Execute](querydef-execute-method-dao.md)** o **[OpenConnection](dbengine-openconnection-method-dao.md)** invocado más recientemente (es decir, un método ejecutado con la opción **dbRunAsync**) se completó. Mientras la propiedad **StillExecuting** esté establecida en **True**, no se puede tener acceso a ningún objeto devuelto.

Una vez que la propiedad **StillExecuting** devuelva **False**, seguido de la llamada **OpenConnection** que devuelve el objeto asociado **[Connection](connection-object-dao.md)**, se puede hacer referencia al objeto. Mientras que **StillExecuting** permanezca establecida en **True**, no se puede hacer referencia al objeto, aparte de leer la propiedad **StillExecuting**.

Utilice el método **[Cancel](connection-cancel-method-dao.md)** para finalizar la ejecución de una tarea que se esté realizando.

