---
title: Crear un elemento de tarea periódica simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345475"
---
# <a name="create-a-simple-recurrent-task-item"></a>Crear un elemento de tarea periódica simple

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI se puede usar para crear elementos de tarea. En este tema se describe cómo crear un elemento de tarea recurrente simple.
  
Para obtener información sobre cómo descargar, ver y ejecutar el código de la aplicación MFCMAPI y el proyecto CreateOutlookItemsAddin al que se hace referencia en este tema, vea [Instalar](how-to-install-the-samples-used-in-this-section.md)los ejemplos usados en esta sección.

### <a name="to-create-a-task-item"></a>Para crear un elemento de tarea

1. Abra un almacén de mensajes. Para obtener información sobre cómo abrir un almacén de mensajes, vea [Abrir un almacén de mensajes.](opening-a-message-store.md)
    
2. Abra la carpeta Tareas en el almacén de mensajes. Para obtener más información, **vea PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Llame al [método IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en la carpeta Tareas para crear el nuevo elemento de tarea. 
    
4. Establezca la **propiedad dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) y otras propiedades relacionadas con tareas necesarias para crear una tarea periódica.
    
5. Guarde el nuevo elemento de tarea.
    
La  `AddTask` función del archivo de origen Tasks.cpp del proyecto CreateOutlookItemsAddin muestra estos pasos. La función toma parámetros del cuadro de diálogo Agregar tarea que se muestra al hacer clic en Agregar tarea en el menú Complementos de la aplicación de ejemplo `AddTask` MFCMAPI.    La función de Tasks.cpp muestra el cuadro de diálogo y pasa valores  `DisplayAddTaskDialog` del cuadro de diálogo a la  `AddTask` función. La función no se relaciona directamente con la creación de un elemento de tarea mediante MAPI, por lo  `DisplayAddTaskDialog` que no se muestra aquí. 
  
> [!IMPORTANT]
> El código de la aplicación MFCMAPI  no garantiza que se  haya seleccionado la carpeta Tareas al hacer clic en el comando Agregar tarea del **menú** Complementos. La creación de elementos de tarea en una carpeta que no sea **la carpeta** Tareas puede provocar un comportamiento no definido. Asegúrese de haber seleccionado la carpeta **Tareas** antes de usar el comando **Agregar** tarea en la aplicación MFCMAPI. 
  
La  `AddTask` función se muestra a continuación. Tenga en cuenta que el parámetro _lpFolder_ pasado a la función es un puntero a una interfaz IMAPIFolder que representa la carpeta donde `AddTask` se crea la nueva tarea. [](imapifolderimapicontainer.md) Dado el _lpFolder_ que representa una **interfaz IMAPIFolder,** el código llama al método [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) El **método CreateMessage** devuelve un código correcto y un puntero a un puntero a una **interfaz IMessage.** La mayor parte del código de función controla el trabajo de especificar propiedades en preparación para llamar al método `AddTask` [IMAPIProp::SetProps.](imapiprop-setprops.md) Si la llamada al método **SetProps** se realiza correctamente, se llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para confirmar los cambios en el almacén y crear un nuevo elemento de tarea. 
  
La  `AddTask` función establece un número de propiedades con nombre. Para obtener información acerca de las propiedades con nombre y cómo se crean, vea Usar MAPI para crear elementos [de Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx). Dado que las propiedades con nombre usadas para los elementos de tarea ocupan varios conjuntos de propiedades, debe tenerse cuidado al crear parámetros para pasar al método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
  
La función usa la función auxiliar para crear una estructura que represente una periodicidad de tarea para establecer `AddTask` `BuildWeeklyTaskRecurrencePattern` la propiedad **dispidTaskRecur.** Para obtener información sobre la estructura de periodicidad de la tarea que genera la función, vea Propiedad canónica  `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) y Propiedad canónica [PidLidRecurrencePattern](pidlidrecurrencepattern-canonical-property.md). 

Tenga en cuenta que aunque una gran variedad de patrones de periodicidad son posibles, la función solo crea  `BuildWeeklyTaskRecurrencePattern` un patrón de periodicidad semanal. También está codificado de forma permanente para una serie de suposiciones, como el tipo de calendario (gregoriano), el primer día de la semana (domingo) y el número de instancias modificadas o eliminadas (ninguna). Una función de creación de patrones de periodicidad de propósito más general tendría que aceptar este tipo de variables como parámetros. 
  
A continuación se muestra la lista completa de la  `AddTask` función. 
  
```cpp
HRESULT AddTask(LPMAPIFOLDER lpFolder,
            SYSTEMTIME* lpstStart, // PidLidCommonEnd, PidLidTaskDueDate, PidLidTaskRecurrence
            SYSTEMTIME* lpstEnd, // PidLidTaskRecurrence
            SYSTEMTIME* lpstFirstDOW, // PidLidTaskRecurrence
            DWORD dwPeriod, // PidLidTaskRecurrence
            DWORD dwOccurrenceCount, // PidLidTaskRecurrence
            DWORD dwPatternTypeSpecific, // PidLidTaskRecurrence
            LPWSTR szSubject, // PR_SUBJECT_W
            LPWSTR szBody) // PR_BODY_W
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulTaskProps];
      LPMAPINAMEID rgpnmid[ulTaskProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulTaskProps ; i++)
      {
         if (i < ulFirstTaskProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Task;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulTaskProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulTaskProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidTaskMode].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskMode],PT_LONG);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidTaskStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskStatus],PT_LONG);
         spvProps[p_PidLidPercentComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidPercentComplete],PT_DOUBLE);
         spvProps[p_PidLidTaskState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskState],PT_LONG);
         spvProps[p_PidLidTaskRecurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskRecurrence],PT_BINARY);
         spvProps[p_PidLidTaskDeadOccurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDeadOccurrence],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwner].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwner],PT_UNICODE);
         spvProps[p_PidLidTaskFRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFRecurring],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwnership].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwnership],PT_LONG);
         spvProps[p_PidLidTaskAcceptanceState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskAcceptanceState],PT_LONG);
         spvProps[p_PidLidTaskFFixOffline].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFFixOffline],PT_BOOLEAN);
         spvProps[p_PidLidTaskDueDate].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDueDate],PT_SYSTIME);
         spvProps[p_PidLidTaskComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskComplete],PT_SYSTIME);
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag   = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag        = PR_ICON_INDEX;
         spvProps[p_PR_SUBJECT_W].ulPropTag         = PR_SUBJECT_W;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag     = PR_MESSAGE_FLAGS;
         spvProps[p_PR_BODY_W].ulPropTag            = PR_BODY_W;
         spvProps[p_PidLidTaskMode].Value.l = tdmtNothing;
         SYSTEMTIME stStartUTC = {0};
         TzSpecificLocalTimeToSystemTime(NULL,lpstStart,&stStartUTC);
         SystemTimeToFileTime(&stStartUTC,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidTaskStatus].Value.l = tsvNotStarted;
         spvProps[p_PidLidPercentComplete].Value.dbl = 0.0;
         spvProps[p_PidLidTaskState].Value.l = tdsOWNNEW;
         spvProps[p_PidLidTaskDeadOccurrence].Value.b = false;
         spvProps[p_PidLidTaskOwner].Value.lpszW = L"Unknown";
         spvProps[p_PidLidTaskFRecurring].Value.b = true;
         spvProps[p_PidLidTaskOwnership].Value.l = tovNew;
         spvProps[p_PidLidTaskAcceptanceState].Value.l = tdvNone;
         spvProps[p_PidLidTaskFFixOffline].Value.b = true;
         SystemTimeToFileTime(lpstStart,&spvProps[p_PidLidTaskDueDate].Value.ft);
         spvProps[p_PidLidTaskComplete].Value.b = false;
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Task";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x501; // Unassigned Recurring Task
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         spvProps[p_PR_BODY_W].Value.lpszW = szBody;
         hRes = BuildWeeklyTaskRecurrencePattern(
            lpstStart,
            lpstEnd,
            lpstFirstDOW,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.cb,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.lpb);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
            if (SUCCEEDED(hRes))
            {
               hRes = lpMessage->SaveChanges(FORCE_SAVE);
            }
         }
         if (spvProps[p_PidLidTaskRecurrence].Value.bin.lpb)
            delete[] spvProps[p_PidLidTaskRecurrence].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a>Consulte también

- [Uso de MAPI para crear elementos de Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

