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
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="96993-103">Crear un elemento de tarea periódica simple</span><span class="sxs-lookup"><span data-stu-id="96993-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="96993-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96993-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96993-105">MAPI se puede usar para crear elementos de tarea.</span><span class="sxs-lookup"><span data-stu-id="96993-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="96993-106">En este tema se describe cómo crear un elemento de tarea simple y recurrente.</span><span class="sxs-lookup"><span data-stu-id="96993-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="96993-107">Para obtener información sobre cómo descargar, ver y ejecutar el código desde la aplicación MFCMAPI y el proyecto CreateOutlookItemsAddin al que se hace referencia en este tema, vea [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="96993-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="96993-108">Para crear un elemento de tarea</span><span class="sxs-lookup"><span data-stu-id="96993-108">To create a task item</span></span>

1. <span data-ttu-id="96993-109">Abra un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96993-109">Open a message store.</span></span> <span data-ttu-id="96993-110">Para obtener información sobre cómo abrir un almacén de mensajes, vea [Opening a Message Store](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="96993-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="96993-111">Abra la carpeta Tareas en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96993-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="96993-112">Para obtener más información, **vea PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96993-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="96993-113">Llame al [método IMAPIFolder::CreateMessage](imapifolder-createmessage.md) en la carpeta Tareas para crear el nuevo elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="96993-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="96993-114">Establezca la **propiedad dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) y otras propiedades relacionadas con tareas necesarias para crear una tarea periódica.</span><span class="sxs-lookup"><span data-stu-id="96993-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="96993-115">Guarde el nuevo elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="96993-115">Save the new task item.</span></span>
    
<span data-ttu-id="96993-116">La  `AddTask` función del archivo de origen Tasks.cpp del proyecto CreateOutlookItemsAddin muestra estos pasos.</span><span class="sxs-lookup"><span data-stu-id="96993-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="96993-117">La función toma parámetros del cuadro de diálogo Agregar tarea que se muestra al hacer clic en Agregar tarea en el menú `AddTask` **Addins** de la aplicación de ejemplo MFCMAPI.  </span><span class="sxs-lookup"><span data-stu-id="96993-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="96993-118">La función tasks.cpp muestra el cuadro de diálogo y pasa los valores  `DisplayAddTaskDialog` del cuadro de diálogo a la  `AddTask` función.</span><span class="sxs-lookup"><span data-stu-id="96993-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="96993-119">La función no se relaciona directamente con la creación de un elemento de tarea con MAPI, por lo  `DisplayAddTaskDialog` que no se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="96993-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="96993-120">El código de la aplicación MFCMAPI  no garantiza que se  haya seleccionado la carpeta Tareas al hacer clic en el comando Agregar tarea del **menú Addins.**</span><span class="sxs-lookup"><span data-stu-id="96993-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="96993-121">La creación de elementos de tarea en una carpeta que no sea **la carpeta Tareas** puede provocar un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="96993-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="96993-122">Asegúrese de haber seleccionado la carpeta **Tareas** antes de usar el comando **Agregar tarea** en la aplicación MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="96993-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="96993-123">La  `AddTask` función se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="96993-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="96993-124">Tenga en cuenta que el parámetro _lpFolder_ pasado a la función es un puntero a una interfaz IMAPIFolder que representa la carpeta donde `AddTask` se crea la nueva tarea. [](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="96993-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="96993-125">Dado el _lpFolder_ que representa una **interfaz IMAPIFolder,** el código llama al [método IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="96993-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="96993-126">El **método CreateMessage** devuelve un código correcto y un puntero a un puntero a una **interfaz IMessage.**</span><span class="sxs-lookup"><span data-stu-id="96993-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="96993-127">La mayoría del código de función controla el trabajo de especificar propiedades como preparación para llamar al `AddTask` [método IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="96993-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="96993-128">Si la llamada al **método SetProps** se realiza correctamente, se llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para confirmar los cambios en el almacén y crear un nuevo elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="96993-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="96993-129">La  `AddTask` función establece un número de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="96993-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="96993-130">Para obtener información sobre las propiedades con nombre y cómo se crean, vea [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="96993-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="96993-131">Dado que las propiedades con nombre usadas para los elementos de tarea ocupan varios conjuntos de propiedades, debe tenerse cuidado al crear parámetros para pasar al método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="96993-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="96993-132">La función usa la función auxiliar para crear una estructura que represente una periodicidad de tarea `AddTask` para establecer la propiedad `BuildWeeklyTaskRecurrencePattern` **dispidTaskRecur.**</span><span class="sxs-lookup"><span data-stu-id="96993-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="96993-133">Para obtener información sobre la estructura de periodicidad de tareas que genera la función, vea  `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) y [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="96993-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="96993-134">Tenga en cuenta que, aunque es posible una gran variedad de patrones de periodicidad, la función solo  `BuildWeeklyTaskRecurrencePattern` crea un patrón de periodicidad semanal.</span><span class="sxs-lookup"><span data-stu-id="96993-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="96993-135">También está codificado de forma permanente para una serie de suposiciones, como el tipo de calendario (gregoriano), el primer día de la semana (domingo) y el número de instancias modificadas o eliminadas (ninguna).</span><span class="sxs-lookup"><span data-stu-id="96993-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="96993-136">Una función de creación de patrones de periodicidad de uso más general tendría que aceptar este tipo de variables como parámetros.</span><span class="sxs-lookup"><span data-stu-id="96993-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="96993-137">A continuación se muestra la lista completa de la  `AddTask` función.</span><span class="sxs-lookup"><span data-stu-id="96993-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="96993-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="96993-138">See also</span></span>

- [<span data-ttu-id="96993-139">Uso de MAPI para crear Outlook de 2007</span><span class="sxs-lookup"><span data-stu-id="96993-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

