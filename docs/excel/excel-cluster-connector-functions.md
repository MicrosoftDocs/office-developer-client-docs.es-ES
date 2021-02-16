---
title: Funciones del conector de clúster de Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408589"
---
# <a name="excel-cluster-connector-functions"></a>Funciones de Conector de clúster de Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Las DLL del conector de clúster de Microsoft Excel 2013 deben implementar las funciones descritas en esta sección.
  
Los valores devueltos mencionados en los temas de referencia de esta sección se definen en el archivo de incluyen sdk, xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Arquitectura del conector de clúster

Excel llama a puntos de entrada en un conector de clúster para transferir llamadas de función definidas por el usuario a un clúster de cálculo de alto rendimiento y para la administración de sesiones de clúster.
  
## <a name="in-this-section"></a>En esta sección

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Consulte también



[Desarrollar conectores clúster de Excel](developing-excel-cluster-connectors.md)
  
[Funciones seguras para clústeres](cluster-safe-functions.md)

