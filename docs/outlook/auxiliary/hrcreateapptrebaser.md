---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Inicializa un objeto IOlkApptRebaser para su uso en reorganización de citas en calendarios de Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397544"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Inicializa un objeto [IOlkApptRebaser](iolkapptrebaser.md) para su uso en reorganización de citas en calendarios de Outlook. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |tzmovelib.dll  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente MAPI  <br/> |
|Tipo de puntero:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Punto de entrada del archivo DLL:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
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

## <a name="parameters"></a>Par�metros

_ulFlags_
  
> [in] Requerido. Una máscara de bits de indicadores que se utilizan para controlar cómo se realiza la modificación de la base. Las siguientes marcas pueden establecerse y se definen en tzmovelib.h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** — se restablecen los elementos de cita en la que el usuario es el organizador de la reunión. Tenga en cuenta que de forma predeterminada, esto hace que Outlook enviar actualizaciones de reunión a todos los asistentes a cualquier reunión que se restablecen. Este indicador se puede combinar con **REBASE_FLAG_FORCE_NO_EX_UPDATES** o **REBASE_FLAG_FORCE_NO_UPDATES** para cambiar cómo se controlan las actualizaciones de la reunión. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** — actualización de elementos de cita que no se han marcado con una zona horaria. Si se especifica este indicador, el valor de *pTZMissing* se usa como la zona horaria que se crea un elemento en todos los elementos que no tienen datos de zona horaria. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — actualizar sólo los elementos de cita periódica. 
    
   - **REBASE_FLAG_NO_UI** : no mostrar cualquier interfaz de usuario (UI), incluidos los cuadros de diálogo de inicio de sesión por lo general que se muestra al abrir un almacén de mensajes. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — no reajustar los elementos de cita que se producen en el pasado. 
    
   - **REBASE_FLAG_FORCE_REBASE** : no comprobar el Organizador para reajustar las decisiones, pero reajustar los elementos de cita en la que el usuario es un asistente. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** : enviar actualizaciones sólo si el usuario es el organizador y el destinatario no está conectado a un servidor de Exchange. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** : no enviar nunca actualizaciones. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** : reajustar sólo los elementos de cita de instancia única creado antes de que se ha aplicado la revisión. 
    
   - **REBASE_FLAG_REPORTING_MODE** — no realmente reajustar, simplemente informe de elementos de cita que debería establecerse en otra ubicación. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** : enviar actualizaciones de reunión a los recursos. 
    
_pSession_
  
> [in] Requerido. Un puntero a una interfaz de sesión MAPI.
    
_pCalendarMsgStore_
  
> [in] Requerido. Un puntero a un almacén de mensajes que contiene los elementos de cita se restablecen.
    
_pCalendarFolder_
  
> [in] Requerido. Un puntero a una carpeta de calendario que contiene los elementos de cita se restablecen.
    
_pwszUpdatePrefix_
  
> [in] Opcional. Un puntero a una cadena que contiene el prefijo que se antepone en las convocatorias de reunión. Puede ser NULL.
    
_pftInstallDateUTC_
  
> [in] Opcional. Fecha de instalación de la revisión de zona horaria. Se usa únicamente si se establece la marca **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** . 
    
_IExpansionDepth_
  
> [in] Opcional. La profundidad de expansión al expandir listas de distribución para excluir a los destinatarios conectado al servidor de Exchange. Sólo se utiliza si se establece la marca **REBASE_FLAG_FORCE_NO_EX_UPDATES** . 
    
_pTZTo_
  
> [in] Requerido. Un puntero a una estructura **TZDEFINITION** que describe la zona horaria que se restablecen a. **TZDEFINITION** se define en tzmovelib. 
    
pTZMissing
  
> [in] Requerido. Un puntero a una estructura **TZDEFINITION** que describe la zona horaria para se supone si no se ha marcado información de zona horaria en un elemento. No debe ser NULL, pero sólo utiliza si se establece la marca **REBASE_FLAG_UPDATE_UNMARKED** . 
    
_ppError_
  
> [out] Un puntero a un puntero a una estructura **MAPIERROR** que contiene información de versión, el componente y el contexto para el error. Puede ser NULL si no hay información de error extendidos se desea obtener. Gratis con [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Un puntero a un puntero a la interfaz devuelta de **IOlkApptRebaser** . 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Cuando se usa [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) para buscar la dirección de esta función en tzmovelib.dll, especifique **HrCreateApptRebaser@44** como el nombre del procedimiento. No todas las marcas son válidos en combinación con cada una de las demás. 
  
Para obtener más información acerca de las distintas opciones, consulte la sección "Glosario de opciones de línea de comandos para la herramienta de actualización de datos de zona horaria de Outlook" en [KB 931667: cómo los cambios de zona horaria de direcciones mediante la herramienta de actualización de datos de zona horaria para Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Vea también

- [Acerca de reajuste mediante programación los calendarios del horario de verano](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

