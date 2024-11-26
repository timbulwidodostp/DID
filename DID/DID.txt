# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Difference-in-Differences (DID) with Multiple Time Periods Use att_gt And aggte (did) With (In) R Software
install.packages("did")
library("did")
DID = read.csv("https://raw.githubusercontent.com/timbulwidodostp/DID/main/DID/DID.csv",sep = ";")
# Estimation Difference-in-Differences (DID) with Multiple Time Periods Use att_gt And aggte (did) With (In) R Software
att_gt <- att_gt(yname = "lemp", gname = "first.treat", idname = "countyreal", tname = "year", xformla = ~1, data = DID, est_method = "reg")
summary(att_gt)
aggte <- aggte(att_gt, type = "dynamic")
summary(aggte)
group_effects <- aggte(att_gt, type = "group")
summary(group_effects)
# Difference-in-Differences (DID) with Multiple Time Periods Use att_gt And aggte (did) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished