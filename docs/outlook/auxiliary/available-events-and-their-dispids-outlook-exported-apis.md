---
title: Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: En esta sección se describe los identificadores de envío para los eventos que Outlook pone a disposición.
ms.openlocfilehash: 1542ff85579346a3674593e9ea38115170df2237
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816066"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)

En esta sección se describe los identificadores de envío para los eventos que Outlook pone a disposición.
  
Outlook expone los siguientes identificadores de envío (DISPID) para permitir que los complementos de C++ escuchar y controlar los eventos correspondientes de la función de [IDispatch:: Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) . 
  
|**Constante**|**Identificador de envío (evento)**|**Descripción**|**Parameters**|**Comentarios**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Se usa para controlar el evento de nivel de la aplicación de la función de **IDispatch:: Invoke** que se desencadena antes de una operación de impresión.  <br/> | Hay 2 parámetros sin nombre:  <br/>  El primer parámetro es del tipo ** VT_BOOL|VT_BREF **. Devolver **VARIANT_TRUE** en este parámetro para cancelar el evento.  <br/>  El segundo parámetro no se utiliza y se debe omitir.  <br/> |Este dispid está disponible desde Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Se usa para controlar el evento de nivel de elemento de la función de **IDispatch:: Invoke** que se desencadena cuando Outlook ha finalizado la lectura de las propiedades del elemento.  <br/> |Hay un solo parámetro _Cancelar_ que es del tipo ** VT_BOOL|VT_BREF **. Devolver **VARIANT_TRUE** en este parámetro para cancelar la operación de lectura.  <br/> |Este dispid está disponible desde Outlook 2010.  <br/> Este evento corresponde al evento las extensiones de cliente de Exchange (ECE) **IExchExtMessageEvents::OnReadComplete**, y también para el evento **ReadComplete** que se ha agregado al modelo de objetos desde Outlook 2013.  <br/> |
   
Para obtener un ejemplo de cómo usar un dispid para escuchar y controlar un evento, vea el `CAppEventListener::Invoke` (función) en la solución de Outlook de C++ se describe en [Implementar receptores de eventos de Outlook 2002/XP en MFC C++ 2003. NET](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Vea también

- [API exportadas de Outlook](outlook-exported-apis.md)
- [Constantes (API exportadas de Outlook)](constants-outlook-exported-apis.md)
- [Información sobre las API exportadas por Outlook](about-apis-exported-by-outlook.md)
- [Implementar eventos de Outlook 2002/XP receptores en MFC C++ .NET 2003](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

