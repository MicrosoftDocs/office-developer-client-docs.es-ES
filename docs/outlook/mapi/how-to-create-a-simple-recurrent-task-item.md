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
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="8ebf6-103">Crear un elemento de tarea periódica simple</span><span class="sxs-lookup"><span data-stu-id="8ebf6-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="8ebf6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ebf6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ebf6-105">MAPI se puede usar para crear para crear elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="8ebf6-106">En este tema se describe cómo crear un elemento de tarea periódica simple.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="8ebf6-107">Para obtener información acerca de cómo descargar, ver y ejecutar el código de la aplicación MFCMAPI y el proyecto de CreateOutlookItemsAddin hace referencia en este tema, vea [instalar los ejemplos que se usa en esta sección](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="8ebf6-108">Para crear un elemento de tarea</span><span class="sxs-lookup"><span data-stu-id="8ebf6-108">To create a task item</span></span>

1. <span data-ttu-id="8ebf6-109">Abra un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-109">Open a message store.</span></span> <span data-ttu-id="8ebf6-110">Para obtener información sobre cómo abrir un almacén de mensajes, vea [Abrir un almacén de mensajes](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="8ebf6-111">Abra la carpeta de tareas en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="8ebf6-112">Para obtener más información, vea **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="8ebf6-113">Llame al método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en la carpeta de tareas para crear el nuevo elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="8ebf6-114">Establecer la propiedad **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) y otras propiedades relacionadas con tareas necesarios para crear una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="8ebf6-115">Guardar el nuevo elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-115">Save the new task item.</span></span>
    
<span data-ttu-id="8ebf6-116">El `AddTask` (función) en el archivo de origen Tasks.cpp del proyecto CreateOutlookItemsAddin muestra estos pasos.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="8ebf6-117">El `AddTask` función toma parámetros desde el cuadro de diálogo **Agregar tarea** que se muestra al hacer clic en **Agregar tarea** en el menú **Addins** en la aplicación de ejemplo MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="8ebf6-118">El `DisplayAddTaskDialog` función en Tasks.cpp muestra el cuadro de diálogo y pasa los valores del cuadro de diálogo para el `AddTask` (función).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="8ebf6-119">El `DisplayAddTaskDialog` función no directamente relacionados con la creación de un elemento de tarea con MAPI, por lo que no se incluye aquí.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8ebf6-120">El código de la aplicación MFCMAPI no garantiza que se ha seleccionado la carpeta de **tareas** al hacer clic en el comando **Agregar tarea** en el menú **Addins** .</span><span class="sxs-lookup"><span data-stu-id="8ebf6-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="8ebf6-121">Creación de elementos de tarea en una carpeta distinta de la carpeta de **tareas** puede causar un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="8ebf6-122">Asegúrese de que ha seleccionado la carpeta de **tareas** antes de usar el comando **Agregar tarea** en la aplicación MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="8ebf6-123">El `AddTask` (función) se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="8ebf6-124">Tenga en cuenta que el parámetro _lpFolder_ se pasa a la `AddTask` función es un puntero a una interfaz [IMAPIFolder](imapifolderimapicontainer.md) que representa la carpeta donde se crea la nueva tarea.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="8ebf6-125">Dada la _lpFolder_ que representa una interfaz **IMAPIFolder** , el código llama al método de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebf6-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="8ebf6-126">El método **CreateMessage** devuelve un código de éxito y un puntero a un puntero a **una interfaz** .</span><span class="sxs-lookup"><span data-stu-id="8ebf6-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="8ebf6-127">La mayoría de los `AddTask` código de función controla el trabajo de especificar las propiedades de la preparación para llamar al método [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebf6-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="8ebf6-128">Si la llamada al método **SetProps** se realiza correctamente, se llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para confirmar los cambios en el almacén y crear un nuevo elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="8ebf6-129">El `AddTask` función establece un número de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="8ebf6-130">Para obtener información acerca de las propiedades con nombre y cómo se crean, vea [Uso de MAPI para crear elementos de Outlook 2007](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="8ebf6-131">Debido a que las propiedades con nombre que se utiliza para los elementos de tarea ocupan varios conjuntos de propiedades, debe tener cuidado al crear parámetros para pasar al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebf6-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="8ebf6-132">El `AddTask` función utiliza la `BuildWeeklyTaskRecurrencePattern` función auxiliar para crear una estructura que representa una periodicidad de la tarea para establecer la propiedad **dispidTaskRecur** .</span><span class="sxs-lookup"><span data-stu-id="8ebf6-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="8ebf6-133">Para obtener información sobre la estructura de periodicidad de la tarea el `BuildWeeklyTaskRecurrencePattern` funcionar compilaciones, vea [Propiedad canónico PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) y [Propiedad canónico PidLidRecurrencePattern](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="8ebf6-134">Tenga en cuenta que mientras una gran variedad de patrones de periodicidad son posibles, el `BuildWeeklyTaskRecurrencePattern` (función), sólo genera un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="8ebf6-135">También es difícil de forma rígida para una serie de supuestos, como el tipo de calendario (gregoriano), el primer día de la semana (domingo) y el número de instancias modificadas o eliminadas (ninguno).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="8ebf6-136">Un uso más general función de creación de patrón de periodicidad tendría que acepte estos tipos de variables como parámetros.</span><span class="sxs-lookup"><span data-stu-id="8ebf6-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="8ebf6-137">La siguiente es una lista completa de la `AddTask` (función).</span><span class="sxs-lookup"><span data-stu-id="8ebf6-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="8ebf6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ebf6-138">See also</span></span>

- [<span data-ttu-id="8ebf6-139">Uso de MAPI para crear elementos de Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="8ebf6-139">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

