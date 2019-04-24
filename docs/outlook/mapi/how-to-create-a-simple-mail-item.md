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
# <a name="create-a-simple-mail-item"></a>Crear un elemento de correo simple
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI se puede usar para crear y enviar un mensaje que solicite una confirmación de lectura. Cuando se solicita una confirmación de lectura, el sistema de mensajería genera y devuelve un informe de lectura al remitente cuando el destinatario abre el mensaje.
  
Para obtener información sobre cómo descargar, ver y ejecutar el código de la aplicación MFCMAPI y el proyecto CreateOutlookItemsAddin a los que se hace referencia en este tema, consulte [instalar los ejemplos que se han usado en esta sección](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Para crear y enviar un mensaje que solicite una confirmación de lectura

1. Cree un mensaje saliente. Para obtener información acerca de cómo crear un mensaje saliente, vea el apartado sobre cómo [controlar un mensaje saliente](handling-an-outgoing-message.md).
    
2. Agregue la propiedad **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) y establezca su valor en **true**.
    
3. Agregue la propiedad **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Agregue la propiedad **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Envíe el mensaje mediante una llamada al método [IMessage:: SubmitMessage](imessage-submitmessage.md) . 
    
La `AddMail` función del archivo de origen de mails. cpp del proyecto CreateOutlookItemsAddin muestra estos pasos. La `AddMail` función toma los parámetros del cuadro de diálogo **Agregar correo** que aparece al hacer clic en el comando **Agregar correo** en **** el menú complementos de la aplicación de ejemplo MFCMAPI. La `DisplayAddMailDialog` función de mails. cpp muestra el cuadro de diálogo y pasa los valores del cuadro de diálogo a `AddMail` la función. La `DisplayAddMailDialog` función no se relaciona directamente con la creación de un elemento de correo mediante MAPI, por lo que no aparece aquí. La `AddMail` función se muestra a continuación. 
  
Tenga en cuenta que el parámetro _lpFolder_ pasado `AddMail` al método es un puntero a una interfaz [IMAPIFolder](imapifolderimapicontainer.md) que representa la carpeta en la que se creará el nuevo mensaje. Según el parámetro _lpFolder_ que representa una interfaz **IMAPIFolder** , el código llama al método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . El método **CreateMessage** devuelve un código de éxito y un puntero a un puntero a una interfaz [IMessage: IMAPIProp](imessageimapiprop.md) . 

La mayor parte `AddMail` del código de la función administra el trabajo de establecer propiedades en preparación para llamar al método [IMAPIProp:: SetProps](imapiprop-setprops.md) . Si la llamada al método **SetProps** se realiza correctamente, una llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) confirma los cambios en el almacén y crea un nuevo elemento de correo. A continuación, si se solicita, se llama al método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar el mensaje. 
  
La `AddMail` función usa dos funciones auxiliares para generar valores para las propiedades **PR_CONVERSATION_INDEX** y **PR_REPORT_TAG** : las `BuildConversationIndex` funciones y `AddReportTag` . La `BuildConversationIndex` función, que se encuentra en CreateOutlookItemsAddin. cpp, realiza el mismo trabajo que la función [ScCreateConversationIndex](sccreateconversationindex.md) de MAPI integrada cuando no se le pasa un índice de conversaciones primario. El formato del búfer de índice de conversaciones que generan estas funciones se documenta en [propiedad canónica PidTagConversationIndex](pidtagconversationindex-canonical-property.md). 

La `AddReportTag` función, que se encuentra en mails. cpp, llama a `BuildReportTag` su vez a la función para compilar una estructura para la propiedad **PR_REPORT_TAG** . Para obtener información acerca de la estructura `BuildReportTag` que genera la función, vea [propiedad canónica PidTagReportTag](pidtagreporttag-canonical-property.md).
  
A continuación se muestra la lista completa de `AddMail` la función. 
  
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

## <a name="see-also"></a>Vea también

- [Uso de MAPI para crear elementos de Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

