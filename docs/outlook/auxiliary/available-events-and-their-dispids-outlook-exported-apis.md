---
title: Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: En esta sección se describen los identificadores de envío de los eventos que Outlook pone a disposición.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316880"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)

En esta sección se describen los identificadores de envío de los eventos que Outlook pone a disposición.
  
Outlook expone los siguientes identificadores de distribución (dispids) para permitir que los complementos de C++ puedan escuchar y controlar los eventos correspondientes de la función [IDispatch::Invoke.](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) 
  
|**Constante**|**Insípido para el evento**|**Descripción**|**Parámetros**|**Comentarios**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Se usa para controlar el evento de nivel de aplicación de la función **IDispatch::Invoke** que se dispara antes de una operación de impresión.  <br/> | Hay 2 parámetros sin nombre:  <br/>  El primer parámetro es del tipo **VT_BOOL|VT_BREF**. Devuelve **VARIANT_TRUE** en este parámetro para cancelar el evento.  <br/>  El segundo parámetro no se usa y debe omitirse.  <br/> |Este dispid está disponible desde Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Se usa para controlar el evento de nivel de elemento de la función **IDispatch::Invoke** que se dispara cuando Outlook ha completado la lectura de las propiedades del elemento.  <br/> |Solo hay un parámetro  _Cancel_ que es del tipo **VT_BOOL|VT_BREF**. Devuelve **VARIANT_TRUE** en este parámetro para cancelar la operación de lectura.  <br/> |Este dispid está disponible desde Outlook 2010.  <br/> Este evento corresponde al evento de extensiones de cliente (ECE) de Exchange **IExchExtMessageEvents::OnReadComplete** y también al evento **ReadComplete** que se ha agregado al modelo de objetos desde Outlook 2013.  <br/> |
   
Para obtener un ejemplo de cómo usar un poco para escuchar y controlar un evento, vea la función de la solución de Outlook de C++ descrita en `CAppEventListener::Invoke` [Implementing Outlook 2002/XP Event Sinks in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Vea también

- [API exportadas de Outlook](outlook-exported-apis.md)
- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [Información sobre las API exportadas por Outlook](about-apis-exported-by-outlook.md)
- [Implementación de Outlook receptores de eventos de 2002/XP en MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

