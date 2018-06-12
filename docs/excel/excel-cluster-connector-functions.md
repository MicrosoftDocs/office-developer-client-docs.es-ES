---
title: Funciones de conector de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815554"
---
# <a name="excel-cluster-connector-functions"></a>Funciones de conector de clúster de Excel

 **Se aplica a**: Excel 2013 | Office 2013 | Visual Studio 
  
Conector de clúster de Microsoft Excel 2013 dll debe implementar las funciones que se describen en esta sección.
  
Los valores devueltos que se mencionan en los temas de esta sección se definen en el SDK de referencia incluyen archivo, xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Arquitectura del conector de clúster

Excel llama a puntos de entrada en un conector de clúster para transferir las llamadas de función definida por el usuario a un clúster de cálculo de alto rendimiento y para la administración de sesiones de clúster.
  
## <a name="in-this-section"></a>En esta sección

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Ver también



[Desarrollo de conectores de cl�ster de Excel de 2013](developing-excel-cluster-connectors.md)
  
[Funciones seguras de clúster](cluster-safe-functions.md)

