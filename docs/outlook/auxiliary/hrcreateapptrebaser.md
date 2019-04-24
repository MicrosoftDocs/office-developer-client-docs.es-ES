---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa un objeto IOlkApptRebaser para su uso en la reajuste de citas en los calendarios de Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317615"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Inicializa un objeto [IOlkApptRebaser](iolkapptrebaser.md) para su uso en la reajuste de citas en los calendarios de Outlook. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib. h  <br/> |
|Implementado por:  <br/> |tzmovelib. dll  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente de MAPI  <br/> |
|Tipo de puntero:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Punto de entrada de DLL:  <br/> |**HrCreateApptRebaser @ 44** <br/> |
   
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

## <a name="parameters"></a>Parameters

_ulFlags_
  
> [in] Requerido. Máscara de la máscara usada para controlar cómo se realiza el reajuste. Se pueden establecer y definir los siguientes indicadores en tzmovelib. h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : elementos de cita en los que el usuario es el organizador de la reunión en el que se rebasa. Tenga en cuenta que, de forma predeterminada, Outlook envía actualizaciones de reunión a todos los asistentes de las reuniones que se rebasen. Puede combinar este indicador con **REBASE_FLAG_FORCE_NO_EX_UPDATES** o **REBASE_FLAG_FORCE_NO_UPDATES** para cambiar la forma en que se administran las actualizaciones de reunión. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** : actualizar elementos de cita que no se han marcado con una zona horaria. Si se especifica este indicador, se usa el valor *pTZMissing* como la zona horaria en la que se crea un elemento para todos los elementos que no tienen datos de zona horaria. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** : actualizar solo los elementos de cita periódicos. 
    
   - **REBASE_FLAG_NO_UI** — no mostrar ninguna interfaz de usuario (UI), incluidos los cuadros de diálogo de inicio de sesión que se suelen mostrar al abrir un almacén de mensajes. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** : no se rebasen los elementos de cita que se produjeron en el pasado. 
    
   - **REBASE_FLAG_FORCE_REBASE** : no comprueba el organizador para las decisiones de reajuste, sino que rebase los elementos de cita en los que el usuario es un asistente. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** : enviar actualizaciones solo si el usuario es el organizador y el destinatario no está conectado a un servidor de Exchange. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** : no enviar nunca actualizaciones. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** : sólo se rebasen los elementos de cita de instancia única creados antes de que se aplicara la revisión. 
    
   - **REBASE_FLAG_REPORTING_MODE** : no se rebasa realmente, solo notificar los elementos de cita que se rebasarían. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** : enviar actualizaciones de reunión a los recursos. 
    
_pSession_
  
> [in] Requerido. Un puntero a una interfaz de sesión MAPI.
    
_pCalendarMsgStore_
  
> [in] Requerido. Un puntero a un almacén de mensajes que contiene elementos de cita que se van a rebasar.
    
_pCalendarFolder_
  
> [in] Requerido. Un puntero a una carpeta de calendario que contiene los elementos de cita que se van a rebasar.
    
_pwszUpdatePrefix_
  
> [in] Opcional. Un puntero a una cadena que contiene el prefijo que se va a anteponer a las convocatorias de reunión. Puede ser NULL.
    
_pftInstallDateUTC_
  
> [in] Opcional. Fecha de instalación de la revisión de la zona horaria. Solo se usa si se establece la marca **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** . 
    
_IExpansionDepth_
  
> [in] Opcional. La profundidad de expansión al expandir las listas de distribución para excluir a los destinatarios conectados a Exchange Server. Solo se usa si se establece la marca **REBASE_FLAG_FORCE_NO_EX_UPDATES** . 
    
_pTZTo_
  
> [in] Requerido. Puntero a una estructura **TZDEFINITION** que describe la zona horaria a la que se va a rebasar. **TZDEFINITION** se define en tzmovelib. 
    
pTZMissing
  
> [in] Requerido. Un puntero a una estructura **TZDEFINITION** que describe la zona horaria que se va a asumir si la información de la zona horaria no se marca en un elemento. No debe ser NULL, pero solo se usa si se ha establecido la marca **REBASE_FLAG_UPDATE_UNMARKED** . 
    
_ppError_
  
> contempla Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, componente y contexto para el error. Puede ser NULL si no se desea ninguna información de error extendida. Gratis con [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> contempla Un puntero a un puntero a la interfaz **IOlkApptRebaser** devuelta. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Al utilizar [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para buscar la dirección de esta función en tzmovelib. dll, especifique **HrCreateApptRebaser @ 44** como nombre del procedimiento. No todas las marcas son válidas en combinación entre sí. 
  
Para obtener más información acerca de las distintas opciones, consulte la sección "Glosario de opciones de línea de comandos para la herramienta de actualizar datos de zona horaria de Outlook" en [KB 931667: Cómo dirigir los cambios de zona horaria mediante la herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

