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
ms.openlocfilehash: 926b33fa3627461139362737f86248f217191534
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816974"
---
# <a name="create-a-simple-recurrent-task-item"></a>Crear un elemento de tarea periódica simple

**Hace referencia a**: Outlook 
  
MAPI se puede usar para crear para crear elementos de tarea. En este tema se describe cómo crear un elemento de tarea periódica simple.
  
Para obtener información acerca de cómo descargar, ver y ejecutar el código de la aplicación MFCMAPI y el proyecto de CreateOutlookItemsAddin hace referencia en este tema, vea [instalar los ejemplos que se usa en esta sección](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-create-a-task-item"></a>Para crear un elemento de tarea

1. Abra un almacén de mensajes. Para obtener información sobre cómo abrir un almacén de mensajes, vea [Abrir un almacén de mensajes](opening-a-message-store.md).
    
2. Abra la carpeta de tareas en el almacén de mensajes. Para obtener más información, vea **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Llame al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en la carpeta de tareas para crear el nuevo elemento de tarea. 
    
4. Establecer la propiedad **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) y otras propiedades relacionadas con tareas necesarios para crear una tarea periódica.
    
5. Guardar el nuevo elemento de tarea.
    
El `AddTask` (función) en el archivo de origen Tasks.cpp del proyecto CreateOutlookItemsAddin muestra estos pasos. El `AddTask` función toma parámetros desde el cuadro de diálogo **Agregar tarea** que se muestra al hacer clic en **Agregar tarea** en el menú **Addins** en la aplicación de ejemplo MFCMAPI. El `DisplayAddTaskDialog` función en Tasks.cpp muestra el cuadro de diálogo y pasa los valores del cuadro de diálogo para el `AddTask` (función). El `DisplayAddTaskDialog` función no directamente relacionados con la creación de un elemento de tarea con MAPI, por lo que no se incluye aquí. 
  
> [!IMPORTANT]
> El código de la aplicación MFCMAPI no garantiza que se ha seleccionado la carpeta de **tareas** al hacer clic en el comando **Agregar tarea** en el menú **Addins** . Creación de elementos de tarea en una carpeta distinta de la carpeta de **tareas** puede causar un comportamiento indefinido. Asegúrese de que ha seleccionado la carpeta de **tareas** antes de usar el comando **Agregar tarea** en la aplicación MFCMAPI. 
  
El `AddTask` (función) se enumeran a continuación. Tenga en cuenta que el parámetro _lpFolder_ se pasa a la `AddTask` función es un puntero a una interfaz [IMAPIFolder](imapifolderimapicontainer.md) que representa la carpeta donde se crea la nueva tarea. Dada la _lpFolder_ que representa una interfaz **IMAPIFolder** , el código llama al método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . El método **CreateMessage** devuelve un código de éxito y un puntero a un puntero a **una interfaz** . La mayoría de los `AddTask` código de función controla el trabajo de especificar las propiedades de la preparación para llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) . Si la llamada al método **SetProps** se realiza correctamente, se llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para confirmar los cambios en el almacén y crear un nuevo elemento de tarea. 
  
El `AddTask` función establece un número de propiedades con nombre. Para obtener información acerca de las propiedades con nombre y cómo se crean, vea [Uso de MAPI para crear elementos de Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx). Debido a que las propiedades con nombre que se utiliza para los elementos de tarea ocupan varios conjuntos de propiedades, debe tener cuidado al crear parámetros para pasar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
El `AddTask` función utiliza la `BuildWeeklyTaskRecurrencePattern` función auxiliar para crear una estructura que representa una periodicidad de la tarea para establecer la propiedad **dispidTaskRecur** . Para obtener información sobre la estructura de periodicidad de la tarea el `BuildWeeklyTaskRecurrencePattern` funcionar compilaciones, vea [Propiedad canónico PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) y [Propiedad canónico PidLidRecurrencePattern](pidlidrecurrencepattern-canonical-property.md). 

Tenga en cuenta que mientras una gran variedad de patrones de periodicidad son posibles, el `BuildWeeklyTaskRecurrencePattern` (función), sólo genera un patrón de periodicidad semanal. También es difícil de forma rígida para una serie de supuestos, como el tipo de calendario (gregoriano), el primer día de la semana (domingo) y el número de instancias modificadas o eliminadas (ninguno). Un uso más general función de creación de patrón de periodicidad tendría que acepte estos tipos de variables como parámetros. 
  
La siguiente es una lista completa de la `AddTask` (función). 
  
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

## <a name="see-also"></a>Vea también

- [Uso de MAPI para crear elementos de Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

