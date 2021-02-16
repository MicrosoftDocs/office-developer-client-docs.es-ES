---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Admite el reabasado de citas en una carpeta de calendario.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410073"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Admite el reabasado de citas en una carpeta de calendario.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |**IUnknown** <br/> |
|Archivo de encabezado:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |tzmovelib.dll  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente MAPI  <br/> |
|Expuesto en:  <br/> |Outlook rebasing (objeto)  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Se inicia una tarea de enumeración de la cita en una carpeta de calendario para buscar las citas que necesitan el reajuste.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Espera de enumeración de la cita en una carpeta de calendario para completar y devuelve una lista de citas esa necesidad de reajuste.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Inicia una tarea para el reabasamiento de citas dada una lista de citas, normalmente obtenida de **EndEnumerateAppointments**.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Espera a que cita el reajuste para completar y recupera los resultados.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

