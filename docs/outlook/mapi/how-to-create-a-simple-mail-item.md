---
title: Crear un elemento de correo simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345196"
---
# <a name="create-a-simple-mail-item"></a><span data-ttu-id="e5896-103">Crear un elemento de correo simple</span><span class="sxs-lookup"><span data-stu-id="e5896-103">Create a simple mail item</span></span>
  
<span data-ttu-id="e5896-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5896-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5896-105">MAPI puede usarse para crear y enviar un mensaje que solicita una confirmación de lectura.</span><span class="sxs-lookup"><span data-stu-id="e5896-105">MAPI can be used to create and send a message that requests a read receipt.</span></span> <span data-ttu-id="e5896-106">Cuando se solicita una confirmación de lectura, el sistema de mensajería genera y devuelve un informe de lectura al remitente cuando el destinatario abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5896-106">When a read receipt is requested, the messaging system generates and returns a read report to the sender when the recipient opens the message.</span></span>
  
<span data-ttu-id="e5896-107">Para obtener información sobre cómo descargar, ver y ejecutar el código de la aplicación MFCMAPI y el proyecto CreateOutlookItemsAddin al que se hace referencia en este tema, vea [Instalar](how-to-install-the-samples-used-in-this-section.md)los ejemplos usados en esta sección.</span><span class="sxs-lookup"><span data-stu-id="e5896-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a><span data-ttu-id="e5896-108">Para crear y enviar un mensaje que solicita una confirmación de lectura</span><span class="sxs-lookup"><span data-stu-id="e5896-108">To create and send a message requesting a read receipt</span></span>

1. <span data-ttu-id="e5896-109">Cree un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="e5896-109">Create an outgoing message.</span></span> <span data-ttu-id="e5896-110">Para obtener información acerca de cómo crear un mensaje saliente, vea [Control de un mensaje saliente.](handling-an-outgoing-message.md)</span><span class="sxs-lookup"><span data-stu-id="e5896-110">For information about how to create an outgoing message, see [Handling an Outgoing Message](handling-an-outgoing-message.md).</span></span>
    
2. <span data-ttu-id="e5896-111">Agregue la **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y estapórela en **true**.</span><span class="sxs-lookup"><span data-stu-id="e5896-111">Add the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property and set it to **true**.</span></span>
    
3. <span data-ttu-id="e5896-112">Agregue la **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e5896-112">Add the **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property.</span></span>
    
4. <span data-ttu-id="e5896-113">Agregue la **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e5896-113">Add the **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="e5896-114">Envíe el mensaje llamando al método [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e5896-114">Send the message by calling the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> 
    
<span data-ttu-id="e5896-115">La  `AddMail` función del archivo de origen Mails.cpp del proyecto CreateOutlookItemsAddin muestra estos pasos.</span><span class="sxs-lookup"><span data-stu-id="e5896-115">The  `AddMail` function in the Mails.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="e5896-116">La función toma parámetros del cuadro de diálogo Agregar correo que se muestra al hacer clic en el comando Agregar correo del menú Complementos de la aplicación de ejemplo `AddMail` MFCMAPI.   </span><span class="sxs-lookup"><span data-stu-id="e5896-116">The  `AddMail` function takes parameters from the **Add Mail** dialog box that is displayed when you click the **Add Mail** command on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="e5896-117">La función mails.cpp muestra el cuadro de diálogo y pasa los valores del cuadro  `DisplayAddMailDialog` de diálogo a la  `AddMail` función.</span><span class="sxs-lookup"><span data-stu-id="e5896-117">The  `DisplayAddMailDialog` function in Mails.cpp displays the dialog box and passes the values from the dialog box to the  `AddMail` function.</span></span> <span data-ttu-id="e5896-118">La función no se relaciona directamente con la creación de un elemento de correo mediante MAPI, por lo  `DisplayAddMailDialog` que no se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="e5896-118">The  `DisplayAddMailDialog` function does not relate directly to creating a mail item using MAPI, so it is not listed here.</span></span> <span data-ttu-id="e5896-119">La  `AddMail` función se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="e5896-119">The  `AddMail` function is listed below.</span></span> 
  
<span data-ttu-id="e5896-120">Tenga en cuenta que el parámetro  _lpFolder_ pasado al método es un puntero a una interfaz  `AddMail` [IMAPIFolder](imapifolderimapicontainer.md) que representa la carpeta donde se creará el nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5896-120">Note that the  _lpFolder_ parameter passed to the  `AddMail` method is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new message will be created.</span></span> <span data-ttu-id="e5896-121">Dado el _parámetro lpFolder_ que representa una **interfaz IMAPIFolder,** el código llama al método [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="e5896-121">Given the  _lpFolder_ parameter that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="e5896-122">El **método CreateMessage** devuelve un código de éxito y un puntero a un puntero a una [interfaz IMessage : IMAPIProp.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="e5896-122">The **CreateMessage** method returns a success code and a pointer to a pointer to an [IMessage : IMAPIProp](imessageimapiprop.md) interface.</span></span> 

<span data-ttu-id="e5896-123">La mayoría del código de función controla el trabajo de establecer propiedades en preparación para llamar al método `AddMail` [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="e5896-123">Most of the  `AddMail` function code handles the work of setting properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="e5896-124">Si la llamada al método **SetProps** se realiza correctamente, una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) confirma los cambios en el almacén y crea un nuevo elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="e5896-124">If the call to the **SetProps** method succeeds, a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method commits the changes to the store and creates a new mail item.</span></span> <span data-ttu-id="e5896-125">A continuación, si se solicita, se llama al método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5896-125">Then, if requested, the [IMessage::SubmitMessage](imessage-submitmessage.md) method is called to send the message.</span></span> 
  
<span data-ttu-id="e5896-126">La función usa dos funciones auxiliares para crear valores para las PR_CONVERSATION_INDEX `AddMail` y **PR_REPORT_TAG** propiedades: las funciones  `BuildConversationIndex` `AddReportTag` y.</span><span class="sxs-lookup"><span data-stu-id="e5896-126">The  `AddMail` function uses two helper functions to build values for the **PR_CONVERSATION_INDEX** and **PR_REPORT_TAG** properties: the  `BuildConversationIndex` and  `AddReportTag` functions.</span></span> <span data-ttu-id="e5896-127">La función, ubicada en CreateOutlookItemsAddin.cpp, realiza el mismo trabajo que la función  `BuildConversationIndex` integrada MAPI [ScCreateConversationIndex](sccreateconversationindex.md) cuando no se le pasa un índice de conversación primario.</span><span class="sxs-lookup"><span data-stu-id="e5896-127">The  `BuildConversationIndex` function, located in CreateOutlookItemsAddin.cpp, does the same work that the built-in MAPI [ScCreateConversationIndex](sccreateconversationindex.md) function does when a parent conversation index is not passed to it.</span></span> <span data-ttu-id="e5896-128">El formato del búfer de índices de conversación que generan estas funciones se documenta en la propiedad canónica [PidTagConversationIndex](pidtagconversationindex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="e5896-128">The format of the conversation index buffer that these functions generate is documented in [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md).</span></span> 

<span data-ttu-id="e5896-129">La  `AddReportTag` función, ubicada en Mails.cpp, a su vez llama a la función para crear una  `BuildReportTag` estructura para la **PR_REPORT_TAG** propiedad.</span><span class="sxs-lookup"><span data-stu-id="e5896-129">The  `AddReportTag` function, located in Mails.cpp, in turn calls the  `BuildReportTag` function to build a structure for the **PR_REPORT_TAG** property.</span></span> <span data-ttu-id="e5896-130">Para obtener información acerca de la estructura que  `BuildReportTag` genera la función, vea [Propiedad canónica PidTagReportTag](pidtagreporttag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="e5896-130">For information about the structure that the  `BuildReportTag` function builds, see [PidTagReportTag Canonical Property](pidtagreporttag-canonical-property.md).</span></span>
  
<span data-ttu-id="e5896-131">A continuación se muestra la lista completa de la  `AddMail` función.</span><span class="sxs-lookup"><span data-stu-id="e5896-131">The following is the complete listing of the  `AddMail` function.</span></span> 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a><span data-ttu-id="e5896-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e5896-132">See also</span></span>

- [<span data-ttu-id="e5896-133">Uso de MAPI para crear elementos de Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="e5896-133">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

