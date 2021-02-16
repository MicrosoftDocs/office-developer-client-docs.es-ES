---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa un objeto IOlkApptRebaser para usarlo en el reabasado de citas en calendarios de Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317615"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Inicializa un objeto [IOlkApptRebaser](iolkapptrebaser.md) para usarlo en el reabasado de citas en calendarios de Outlook. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |tzmovelib.dll  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente MAPI  <br/> |
|Tipo de puntero:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Punto de entrada de DLL:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>Parámetros

_ulFlags_
  
> [in] Requerido. Máscara de bits de marcas que se usa para controlar cómo se realiza el reabasamiento. Las siguientes marcas se pueden establecer y definir en tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS:** se rebasen los elementos de cita en los que el usuario es el organizador de la reunión. Tenga en cuenta que, de forma predeterminada, Esto hace que Outlook envíe actualizaciones de reunión a todos los asistentes de cualquier reunión que se rebase. Puede combinar esta marca con REBASE_FLAG_FORCE_NO_EX_UPDATES **o** **REBASE_FLAG_FORCE_NO_UPDATES** para cambiar el modo en que se controlan las actualizaciones de reuniones. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED:** actualice los elementos de cita que no se han marcado con una zona horaria. Si se especifica esta marca, el valor  *pTZMissing*  se usa como la zona horaria en la que se crea un elemento para todos los elementos que no tienen datos de zona horaria. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING:** actualice solo los elementos de citas periódicas. 
    
   - **REBASE_FLAG_NO_UI:** no mostrar ninguna interfaz de usuario (UI), incluidos los cuadros de diálogo de inicio de sesión que se muestran generalmente al abrir un almacén de mensajes. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS:** no vuelva a base los elementos de cita que se producen en el pasado. 
    
   - **REBASE_FLAG_FORCE_REBASE:** no compruebe al organizador si hay decisiones de reebase, sino que vuelva a base los elementos de cita en los que el usuario es un asistente. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES:** envíe actualizaciones solo si el usuario es el organizador y el destinatario no está conectado a un Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES:** no enviar actualizaciones nunca. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH:** vuelva a base solo los elementos de cita de instancia única creados antes de aplicar la revisión. 
    
   - **REBASE_FLAG_REPORTING_MODE:** no vuelva a base, solo informe de los elementos de cita que se rebasen. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES:** enviar actualizaciones de reuniones a los recursos. 
    
_pSession_
  
> [in] Requerido. Puntero a una interfaz de sesión MAPI.
    
_pCalendarMsgStore_
  
> [in] Requerido. Puntero a un almacén de mensajes que contiene los elementos de cita que se van a volver a base.
    
_pCalendarFolder_
  
> [in] Requerido. Puntero a una carpeta de calendario que contiene los elementos de cita que se van a volver a base.
    
_pwszUpdatePrefix_
  
> [in] Opcional. Puntero a una cadena que contiene el prefijo que se debe anteponer a las solicitudes de reunión. Puede ser NULL.
    
_pftInstallDateUTC_
  
> [in] Opcional. Fecha de instalación de la revisión de zona horaria. Solo se usa **si se REBASE_FLAG_ONLY_CREATED_PRE_PATCH** marca de configuración. 
    
_IExpansionDepth_
  
> [in] Opcional. Profundidad de expansión al expandir listas de distribución para excluir los destinatarios conectados a Exchange Server. Solo se usa si **se REBASE_FLAG_FORCE_NO_EX_UPDATES** marca. 
    
_pTZTo_
  
> [in] Requerido. Puntero a una **estructura TZDEFINITION** que describe la zona horaria en la que se va a volver a base. **TZDEFINITION** se define en tzmovelib. 
    
pTZMissing
  
> [in] Requerido. Puntero a una **estructura TZDEFINITION** que describe la zona horaria que se debe asumir si la información de zona horaria no se marca en un elemento. No debe ser NULL, sino que solo se usa si se **REBASE_FLAG_UPDATE_UNMARKED** marca. 
    
_ppError_
  
> [salida] Puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, componente y contexto del error. Puede ser NULL si no se desea ninguna información de error extendida. Libre con [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [salida] Puntero a un puntero a la interfaz **IOlkApptRebaser devuelta.** 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Al usar [GetProcAddress para](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) buscar la dirección de esta función en tzmovelib.dll, especifique **HrCreateApptRebaser@44** como nombre del procedimiento. No todas las marcas son válidas en combinación entre sí. 
  
Para obtener más información acerca de las distintas opciones, vea la sección "Glosario de opciones de línea de comandos para la herramienta de actualización de datos de zona horaria de Outlook" en [KB 931667:](https://support.microsoft.com/kb/931667/en-us)Cómo solucionar los cambios de zona horaria mediante la Herramienta de actualización de datos de zona horaria para Microsoft Office Outlook .
  
## <a name="see-also"></a>Consulte también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

